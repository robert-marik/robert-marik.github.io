---
title: Python v Dockeru
author: Robert Mařík
date: 2026-11-20
layout: post
permalink: navody/docker-micromamba
---

> **⚠️ Upozornění:** Tento dokument byl vygenerován umělou inteligencí a může obsahovat chyby. Použití uvedených příkazů je na vlastní nebezpečí.
{: .block-danger }

Návod na vývojové prostředí pro Python v kontejneru Docker, kde se
závislosti (včetně balíčků z conda-forge, například GDAL) instalují
micromambou a kód i data zůstávají na lokálním disku. Předpokládá se
nainstalovaný [Docker](/navody/docker) s pluginem Compose (`docker compose version`)
a Linux jako hostitelský systém.

## 1. Princip

Kód i data zůstávají na lokálním disku a do kontejneru se připojí jako
*bind mount*. Editor, git a soubory používáte lokálně, kontejner poskytuje
jen Python a závislosti nainstalované micromambou.

Image se přestavuje jen při změně závislostí. Změny kódu jsou
v kontejneru vidět okamžitě, bez buildu.

## 2. Struktura projektu

```text
muj-projekt/
├── docker-compose.yml
├── Dockerfile
├── environment.yml
├── .env
├── .dockerignore
├── src/            # váš kód
└── data/           # data (nebo libovolný jiný adresář na disku)
```

## 3. Konfigurační soubory

### environment.yml

Všechny závislosti, včetně pip balíčků. Název `base` je záměrný,
prostředí se pak v kontejneru aktivuje automaticky.

```yaml
name: base
channels:
  - conda-forge
dependencies:
  - python=3.12
  - numpy
  - pandas
  - gdal
  - pip
  - pip:
      - nejaky-pip-balicek
```

### Dockerfile

Založený na oficiálním image `mambaorg/micromamba`, který je malý
a rychlý.

```dockerfile
FROM mambaorg/micromamba:1.5.10

COPY --chown=$MAMBA_USER:$MAMBA_USER environment.yml /tmp/environment.yml
RUN micromamba install -y -n base -f /tmp/environment.yml && \
    micromamba clean --all --yes

# aby python fungoval i v "docker compose exec" bez aktivace
ENV PATH=/opt/conda/bin:$PATH
# kontejner běží pod vaším UID, které v image nemá domovský adresář
ENV HOME=/tmp
ENV PYTHONUNBUFFERED=1
ENV PYTHONPATH=/workspace/src

WORKDIR /workspace
```

> **Tip:** Verzi image připněte na konkrétní tag, aby se prostředí
> nečekaně neměnilo. Aktuální tagy (včetně řady 2.x) najdete na
> [Docker Hubu](https://hub.docker.com/r/mambaorg/micromamba/tags).
> Cesta `/opt/conda` zůstává stejná.

Systémové programy se instalují přes `USER root`,
`RUN apt-get update && apt-get install -y ...` a zpět `USER $MAMBA_USER`.
Většina potřebných programů je ale dostupná i na conda-forge.

### docker-compose.yml

```yaml
services:
  app:
    build: .
    image: muj-projekt-dev
    user: "${UID:-1000}:${GID:-1000}"
    shm_size: "8gb"                   # víc sdílené paměti pro multiprocessing
    volumes:
      - ./:/workspace                 # kód
      - ${DATA_DIR:-./data}:/data     # data
    working_dir: /workspace
    command: sleep infinity           # kontejner běží a příkazy se do něj posílají
    # ports:
    #   - "8888:8888"                 # odkomentujte pro Jupyter
```

### .env

Compose tento soubor načte automaticky. UID a GID zjistíte příkazy
`id -u` a `id -g`. Bez nich by soubory vytvořené kontejnerem nepatřily
vám.

```bash
UID=1000
GID=1000
DATA_DIR=/home/vase_jmeno/velka_data
```

### .dockerignore

Data a git do image nepatří, jinak se build zbytečně zpomalí.

```text
data/
.git/
__pycache__/
```

## 4. Spuštění a každodenní práce

```bash
docker compose up -d --build      # poprvé: build image a spuštění
docker compose exec app python src/zpracuj.py /data/vstup.csv
docker compose exec app bash      # interaktivní shell v kontejneru
docker compose down               # zastavení
```

Jednorázové spuštění bez běžícího kontejneru:

```bash
docker compose run --rm app python src/zpracuj.py
```

Alias do `~/.bashrc`, aby to působilo jako lokální Python (funguje
v adresáři projektu):

```bash
alias dpy='docker compose exec app python'
# pak stačí: dpy src/zpracuj.py
```

Kód upravujete v lokálním editoru a změny jsou v kontejneru vidět hned.
Po přidání balíčku do `environment.yml` spusťte znovu
`docker compose up -d --build`.

### Napojení editoru

- **VS Code:** rozšíření Dev Containers, příkaz „Reopen in Container“
  a výběr `docker-compose.yml` a služby `app`. Rozšíření vytvoří soubor
  `.devcontainer/devcontainer.json`. Doplňování kódu, debugger i terminál
  pak používají Python z kontejneru.
- **PyCharm Professional:** Settings → Python Interpreter → Add
  Interpreter → Docker Compose, služba `app`.

## 5. Výkon na Linuxu

Výkonnostní ztráta je na Linuxu prakticky zanedbatelná. Kontejner není
virtuální stroj, ale obyčejný proces na hostitelském jádře, izolovaný
pomocí namespaces a cgroups.

| Oblast | Dopad | Poznámka |
| --- | --- | --- |
| CPU a paměť | prakticky žádný | Docker standardně nenastavuje limity, kontejner vidí všechna jádra i celou RAM |
| Bind mounty (`/workspace`, `/data`) | žádný | čtení i zápis jdou přímo na lokální filesystém; pomalost se týká jen macOS a Windows |
| Vnitřní filesystém kontejneru (overlay) | mírný | při tomto nastavení se skoro nepoužívá |
| GPU (NVIDIA) | prakticky žádný | vyžaduje NVIDIA Container Toolkit a v compose sekci `deploy.resources.reservations.devices` |
| Síť (bridge) | malá režie | pro zpracování dat nepodstatná, případně `network_mode: host` |
| Start příkazu přes `exec` | cca 100–300 ms | znát jen u stovek krátkých spuštění |

### Na co si dát pozor

- **Sdílená paměť:** výchozí `/dev/shm` má jen 64 MB. To vadí knihovnám
  s `multiprocessing` nebo sdílenou pamětí (PyTorch DataLoader, Ray,
  joblib). Proto je v compose `shm_size`, alternativně `ipc: host`.
- **Numerické knihovny:** rozdíl ve výkonu obvykle nezpůsobuje Docker,
  ale jiná knihovna BLAS (OpenBLAS místo MKL) nebo jiná verze balíčku.
  Na procesorech Intel může u lineární algebry pomoci přidat do
  `environment.yml` balíček `libblas=*=*mkl`.
- **Krátké opakované příkazy:** smyčku přes stovky souborů je lepší
  udělat uvnitř Pythonu nebo v shellu v kontejneru než opakovaným
  `docker compose exec`.

## 6. Tipy

- **Jupyter:** přidejte `jupyterlab` do `environment.yml`, odkomentujte
  porty v compose a kontejner znovu vytvořte (`docker compose up -d --build`).
  Pak spusťte
  `docker compose exec app jupyter lab --ip=0.0.0.0 --no-browser`
  a otevřete odkaz s tokenem z výpisu.
- **Cesty v kódu:** používejte `/data/...`, případně cestu předávejte
  argumentem nebo proměnnou prostředí. Kde data fyzicky leží, se pak
  mění jen v `DATA_DIR` v `.env`.
- **Úklid:** staré image a mezivrstvy z buildů odstraníte příkazem
  `docker image prune`.

## Další zdroje

* Dokumentace micromamby: <https://mamba.readthedocs.io/en/latest/user_guide/micromamba.html>
* Image micromamba-docker: <https://micromamba-docker.readthedocs.io/>
* Docker Compose: <https://docs.docker.com/compose/>
* Alternativa bez condy: [uv – správce Pythonu a projektů](/navody/uv)
