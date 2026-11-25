---
title: Docker
author: Robert Mařík
date: 2026-11-25
layout: post
permalink: navody/docker
---

Přehled instalace Dockeru, nastavení práv uživatele, práce s Docker
Compose a hlavně uvolňování místa na disku, které Docker rád zabírá.
Příkazy počítají s Ubuntu 22.04 / 24.04 a spouštěním přes `sudo`.

## 1. Instalace

Doporučená cesta je oficiální repozitář Dockeru (balíček `docker.io`
z Ubuntu bývá starší a bez pluginu Compose v2).

Nejprve odstraňte případné staré či konfliktní balíčky:

```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 \
           podman-docker containerd runc; do
  sudo apt remove -y $pkg
done
```

Přidání repozitáře a klíče:

```bash
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg \
     -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] \
https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" \
  | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Instalace:

```bash
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io \
                 docker-buildx-plugin docker-compose-plugin
```

Spuštění služby a zapnutí po startu systému (na Ubuntu se obvykle
stane automaticky):

```bash
sudo systemctl enable --now docker
```

Ověření:

```bash
sudo docker run hello-world
docker --version
docker compose version
```

> **Rychlá varianta:** skript `curl -fsSL https://get.docker.com | sh`
> udělá totéž automaticky. Hodí se na testovací stroje, na produkci je
> lepší vědět, co se instaluje.

## 2. Přidání uživatele do skupiny docker

Bez toho je nutné psát před každý příkaz `sudo`.

```bash
sudo usermod -aG docker $USER
```

Změna skupin se projeví až po novém přihlášení. Pro aktuální terminál
stačí:

```bash
newgrp docker
```

Ověření:

```bash
groups            # ve výpisu musí být docker
docker ps         # musí fungovat bez sudo
```

Jiného uživatele přidáte stejně: `sudo usermod -aG docker jmeno`.
Odebrání ze skupiny: `sudo gpasswd -d jmeno docker`.

> **Pozor:** Členství ve skupině `docker` je fakticky ekvivalent práv
> roota (kontejner může připojit celý disk hostitele). Přidávejte jen
> důvěryhodné uživatele. Alternativou je
> [rootless režim](https://docs.docker.com/engine/security/rootless/).

Pokud se po přidání objeví chyba
`permission denied ... /var/run/docker.sock`, nebyl uživatel znovu
přihlášen. Jestliže dříve spouštěl docker přes `sudo`, může mít
`~/.docker` vlastněný rootem: `sudo chown -R $USER:$USER ~/.docker`.

## 3. Docker Compose

Příkazy se spouštějí v adresáři, kde je `docker-compose.yml`
(nebo `compose.yaml`). Používá se plugin `docker compose` (s mezerou),
starý samostatný `docker-compose` (s pomlčkou) je zastaralý.

### Spuštění

```bash
docker compose up             # na popředí, Ctrl+C zastaví
docker compose up -d          # na pozadí (detached)
docker compose up -d --build  # nejdřív přestaví image
docker compose up -d sluzba   # jen jedna služba (a její závislosti)
```

### Stav a logy

```bash
docker compose ps             # běžící služby projektu
docker compose ps -a          # i zastavené
docker compose logs           # logy všech služeb
docker compose logs -f sluzba # průběžně sledovat jednu službu
docker compose logs --tail 100
docker compose top            # procesy v kontejnerech
```

### Zastavení a odstranění

```bash
docker compose stop           # zastaví kontejnery, nechá je existovat
docker compose start          # znovu spustí zastavené
docker compose restart        # restart (bez načtení změn v yml)
docker compose down           # zastaví a smaže kontejnery a síť
docker compose down -v        # ... a navíc volumes (smaže data!)
docker compose down --rmi all # ... a navíc image projektu
```

Rozdíl: `stop` kontejnery jen zastaví, `down` je odstraní.
Změny v `docker-compose.yml` se projeví po `docker compose up -d`
(změněné služby se vytvoří znovu), `restart` je nenačte.

### Další užitečné příkazy

```bash
docker compose pull                  # stáhne novější verze image
docker compose pull && docker compose up -d   # aktualizace
docker compose build                 # jen build image
docker compose build --no-cache      # build bez cache
docker compose exec sluzba bash      # shell v běžícím kontejneru
docker compose run --rm sluzba cmd   # jednorázový příkaz v novém kontejneru
docker compose config                # výsledná konfigurace (kontrola yml)
docker compose -f jiny.yml up -d     # jiný soubor
docker compose -p nazev up -d        # vlastní název projektu
docker compose ls                    # všechny compose projekty v systému
```

### Spuštění po restartu počítače

Kontejnery se po rebootu spustí samy, pokud mají v `docker-compose.yml`
politiku restartu a služba docker je povolená
(`systemctl enable docker`):

```yaml
services:
  web:
    image: nginx
    restart: unless-stopped
```

`unless-stopped` znamená: spouštět vždy, kromě případu, kdy byl kontejner
ručně zastaven (`docker compose stop`).

## 4. Uvolnění místa na disku

Docker ukládá data do `/var/lib/docker` a postupně se tam hromadí
staré image, zastavené kontejnery, volumes, build cache a logy.

### Kolik místa co zabírá

```bash
docker system df       # souhrn: images, containers, volumes, build cache
docker system df -v    # podrobně po jednotlivých položkách
sudo du -sh /var/lib/docker
```

Sloupec `RECLAIMABLE` ukazuje, kolik lze uvolnit.

Všechny příkazy `prune` se před smazáním ptají na potvrzení,
přepínač `-f` (`--force`) dotaz vynechá. Na konci vypíšou, kolik místa
uvolnily.

### Kontejnery

```bash
docker ps -a                       # všechny kontejnery včetně zastavených
docker container prune             # smaže všechny zastavené kontejnery
docker container prune --filter "until=24h"   # jen zastavené déle než 24 h
docker rm nazev_nebo_id            # konkrétní zastavený kontejner
docker rm -f nazev_nebo_id         # i běžící (zastaví a smaže)
docker rm -f $(docker ps -aq)      # VŠECHNY kontejnery, i běžící
```

Velikost zapisovatelné vrstvy kontejnerů: `docker ps -as`.

### Image

```bash
docker images                      # seznam image
docker image prune                 # jen „dangling“ (<none>:<none>)
docker image prune -a              # všechny image bez kontejneru
docker image prune -a --filter "until=168h"   # nepoužívané starší 7 dní
docker rmi nazev:tag               # konkrétní image
docker rmi $(docker images -q -f dangling=true)
docker rmi -f $(docker images -q)  # VŠECHNY image
```

*Dangling* image jsou bezejmenné zbytky po přestavění image se stejným
tagem. `-a` smaže i pojmenované image, které nepoužívá žádný kontejner
(ani zastavený), takže se při příštím spuštění budou stahovat znovu.

### Volumes

> **Pozor:** Ve volumes bývají data (databáze apod.). Smazání je
> nevratné.

```bash
docker volume ls
docker volume ls -f dangling=true  # volumes bez kontejneru
docker volume prune                # nepoužívané anonymní volumes
docker volume prune -a             # nepoužívané i pojmenované volumes
docker volume rm nazev             # konkrétní volume
```

Od Dockeru 23.0 maže `docker volume prune` jen anonymní volumes,
pojmenované (např. `db_data` z compose) až s `-a`.

### Sítě

```bash
docker network ls
docker network prune               # nepoužívané uživatelské sítě
docker network rm nazev
```

Sítě zabírají zanedbatelné místo, ale hromadí se a mohou kolidovat
rozsahy IP adres.

### Build cache

Při častém buildování bývá build cache největší položkou.

```bash
docker builder prune               # nepoužívaná (dangling) build cache
docker builder prune -a            # veškerá build cache
docker builder prune --filter "until=72h"     # starší než 3 dny
docker builder prune --keep-storage 5GB       # ponechat max. 5 GB
docker buildx prune -a             # totéž pro buildx buildery
docker buildx du                   # využití cache po položkách
```

Novější verze buildx místo `--keep-storage` používají `--max-used-space`.

### Všechno najednou

```bash
docker system prune                # zastavené kontejnery, nepoužívané sítě,
                                   # dangling image, dangling build cache
docker system prune -a             # + všechny nepoužívané image a celá build cache
docker system prune -a --volumes   # + nepoužívané anonymní volumes
docker system prune -af --filter "until=168h" # bez dotazu, jen starší 7 dní
```

`--filter until` nelze kombinovat s `--volumes`.

### Jeden compose projekt

V adresáři projektu:

```bash
docker compose down --rmi all -v --remove-orphans
```

Smaže kontejnery, sítě, image a volumes projektu (`--remove-orphans`
i kontejnery služeb, které už v yml nejsou). Bez `-v` data ve volumes
zůstanou, `--rmi local` smaže jen image bez vlastního tagu (buildované
projektem).

### Logy kontejnerů

Výchozí ovladač `json-file` nemá limit a logy mohou narůst na desítky GB.

```bash
# velikost logů
sudo sh -c 'du -h /var/lib/docker/containers/*/*-json.log' | sort -h

# vyprázdnění logu jednoho kontejneru (kontejner může běžet)
{% raw %}sudo truncate -s 0 $(docker inspect --format='{{.LogPath}}' nazev){% endraw %}

# vyprázdnění všech logů
sudo sh -c 'truncate -s 0 /var/lib/docker/containers/*/*-json.log'
```

Trvalé omezení velikosti v `/etc/docker/daemon.json`:

```json
{
  "log-driver": "json-file",
  "log-opts": {
    "max-size": "10m",
    "max-file": "3"
  }
}
```

```bash
sudo systemctl restart docker
```

Platí jen pro nově vytvořené kontejnery (`docker compose up -d
--force-recreate`). Pro jednu službu lze totéž nastavit
v `docker-compose.yml`:

```yaml
services:
  web:
    image: nginx
    logging:
      options:
        max-size: "10m"
        max-file: "3"
```

### Úplný reset Dockeru

Smaže úplně vše: kontejnery, image, volumes, sítě i cache.

```bash
sudo systemctl stop docker docker.socket containerd
sudo rm -rf /var/lib/docker /var/lib/containerd
sudo systemctl start docker
```

### Přesun dat na jiný disk

Pokud místo dochází trvale, lze data přesunout na větší disk. Do
`/etc/docker/daemon.json` přidejte `"data-root": "/mnt/velky-disk/docker"`,
zastavte docker, zkopírujte data (`sudo rsync -aP /var/lib/docker/
/mnt/velky-disk/docker/`) a spusťte docker znovu.

### Automatické čištění

Týdenní úklid nepoužívaných objektů starších 7 dní přes cron
(`sudo crontab -e`):

```text
0 3 * * 0 /usr/bin/docker system prune -af --filter "until=168h" > /dev/null
```

### Shrnutí

| Co chci smazat | Příkaz |
|---|---|
| zjistit, co zabírá místo | `docker system df -v` |
| zastavené kontejnery | `docker container prune` |
| dangling image | `docker image prune` |
| všechny nepoužívané image | `docker image prune -a` |
| nepoužívané volumes (anonymní / všechny) | `docker volume prune` / `-a` |
| nepoužívané sítě | `docker network prune` |
| build cache | `docker builder prune -a` |
| vše nepoužívané kromě volumes | `docker system prune -a` |
| vše nepoužívané včetně volumes | `docker system prune -a --volumes` |
| jeden compose projekt | `docker compose down --rmi all -v` |
| logy kontejnerů | `truncate -s 0` + `log-opts` v `daemon.json` |
| úplně všechno | smazat `/var/lib/docker` a `/var/lib/containerd` |

Související návod: [Python v Dockeru](/navody/docker-micromamba).
