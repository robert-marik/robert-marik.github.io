---
title: fail2ban na Ubuntu
author: Robert Mařík
date: 2026-11-20
layout: post
permalink: navody/fail2ban
---

Rychlý přehled instalace, konfigurace, kontroly a reportování nástroje
fail2ban, který podle záznamů v logu dočasně blokuje IP adresy útočníků
(typicky při hádání hesel přes SSH). Příkazy počítají s Ubuntu 22.04 /
24.04 a spouštěním přes `sudo`.

## 1. Instalace

```bash
sudo apt update
sudo apt install fail2ban python3-systemd
```

Balíček `python3-systemd` je potřeba pro čtení logů ze systemd journalu
(`backend = systemd`). Po instalaci na Ubuntu je ve výchozím stavu zapnutý
jail `sshd` (soubor `/etc/fail2ban/jail.d/defaults-debian.conf`).

> **Pozor:** Na Ubuntu 24.04 mějte balíček fail2ban aktualizovaný
> (`sudo apt upgrade`). Původní verze z vydání systému se s Pythonem 3.12
> nemusela spustit.

## 2. Spuštění a správa služby

```bash
sudo systemctl enable --now fail2ban   # zapnout při startu + spustit hned
sudo systemctl status fail2ban         # stav služby
sudo systemctl restart fail2ban        # plný restart (bany se obnoví z databáze)
sudo systemctl stop fail2ban           # zastavit
sudo fail2ban-client reload            # znovu načíst konfiguraci bez restartu
sudo fail2ban-client reload sshd       # znovu načíst jen jeden jail
```

## 3. Konfigurace

**Zlaté pravidlo:** nikdy needitujte `/etc/fail2ban/jail.conf` ani
`fail2ban.conf`, při aktualizaci se přepíšou. Vlastní nastavení patří do:

- `/etc/fail2ban/jail.local`, nebo
- `/etc/fail2ban/jail.d/*.local` (přehlednější, jeden soubor na téma).

Pořadí načítání: `jail.conf` → `jail.d/*.conf` → `jail.local` →
`jail.d/*.local`. Pozdější soubor přepisuje dřívější.

### Příklad `/etc/fail2ban/jail.local`

Komentáře pište na **samostatné řádky**. Text za hodnotou na stejném
řádku nemusí být bezpečně rozpoznán jako komentář.

```ini
[DEFAULT]
# IP adresy, které se nikdy nebanují (localhost, domácí síť, vlastní VPN...)
ignoreip = 127.0.0.1/8 ::1 192.168.1.0/24

# jak dlouho ban trvá
bantime  = 1h
# okno, ve kterém se počítají chyby
findtime = 10m
# počet chyb v okně, po kterém následuje ban
maxretry = 5

# Postupně prodlužovat ban opakovaným útočníkům
bantime.increment = true
bantime.factor    = 2
bantime.maxtime   = 5w

[sshd]
enabled  = true
# pokud SSH běží na jiném portu, uveďte jeho číslo, např. 2222
port     = ssh
# logy SSH se čtou ze systemd journalu
backend  = systemd
maxretry = 3
bantime  = 2h

# Ban recidivistů: kdo je zabanovaný opakovaně, dostane týden.
# Čte vlastní log fail2banu, proto potřebuje souborový backend.
[recidive]
enabled  = true
backend  = auto
logpath  = /var/log/fail2ban.log
bantime  = 1w
findtime = 1d
maxretry = 3
```

Po úpravě:

```bash
sudo fail2ban-client -t        # otestuje syntaxi konfigurace
sudo systemctl restart fail2ban
```

## 4. Volby, které je dobré pohlídat

| Volba | K čemu je | Na co si dát pozor |
| --- | --- | --- |
| `ignoreip` | Seznam nikdy nebanovaných IP adres a sítí | Přidejte svou IP a správcovskou síť, jinak se můžete zamknout. Hodnoty oddělujte mezerou. |
| `bantime` | Délka banu | `-1` = trvalý ban (opatrně, seznam banů roste). |
| `findtime` | Časové okno pro počítání chyb | Příliš krátké okno propustí pomalé útoky. |
| `maxretry` | Počet chyb do banu | Příliš nízká hodnota může zabanovat i uživatele s překlepem. |
| `bantime.increment` | Postupně rostoucí ban | Velmi účinné proti botům, kteří se vracejí. |
| `backend` | Odkud se čtou logy (`auto`, `systemd`, `polling`) | Pro SSH je na moderním Ubuntu nejspolehlivější `systemd`. |
| `port` | Chráněný port | U SSH na jiném portu **musí** odpovídat, jinak ban nic neblokuje. |
| `logpath` | Cesta k logu (u souborových backendů) | Neexistující soubor = jail se nespustí. |
| `banaction` | Čím se blokuje (`iptables-multiport`, `nftables`, `ufw`...) | Musí odpovídat firewallu, který opravdu používáte. |
| `mode` (u `sshd`) | `normal` / `ddos` / `extra` / `aggressive` | `aggressive` zachytí nejvíce typů útoků. |
| `destemail`, `action` | E-mailové notifikace | Vyžaduje funkční poštovní server (např. postfix). |
| `enabled` | Zapnutí jailu | Bez `enabled = true` jail neběží. |

## 5. Kontrola, že vše běží

```bash
sudo systemctl status fail2ban          # služba je active (running)?
sudo systemctl is-enabled fail2ban      # startuje po bootu?
sudo fail2ban-client ping               # odpověď: Server replied: pong
sudo fail2ban-client status             # seznam aktivních jailů
sudo fail2ban-client status sshd        # detail jailu
sudo fail2ban-client -t                 # test konfigurace
sudo journalctl -u fail2ban -n 50       # poslední záznamy služby
sudo tail -f /var/log/fail2ban.log      # živý log
```

Ověření, že ban opravdu blokuje na firewallu:

```bash
sudo iptables -L -n | grep -A5 f2b       # iptables
sudo nft list ruleset | grep -A5 f2b     # nftables
```

## 6. Report: co se děje a koho jsme zabanovali

```bash
# Souhrn jailu: počet selhání, počet banů, aktuální seznam IP
sudo fail2ban-client status sshd

# Jen seznam aktuálně zabanovaných IP
sudo fail2ban-client get sshd banip

# Všechny aktuální bany napříč jaily
sudo fail2ban-client banned

# Historie banů z logu
sudo grep " Ban " /var/log/fail2ban.log

# Počet banů za dnešek
sudo grep "$(date +%Y-%m-%d)" /var/log/fail2ban.log | grep -c " Ban "

# Top 10 nejčastěji banovaných IP
sudo grep " Ban " /var/log/fail2ban.log | awk '{print $NF}' | sort | uniq -c | sort -rn | head -n 10

# Včetně rotovaných (i zkomprimovaných) logů
sudo zgrep -h " Ban " /var/log/fail2ban.log*
```

Ukázka výstupu `status sshd`:

```text
Status for the jail: sshd
|- Filter
|  |- Currently failed: 2
|  |- Total failed:     341
|  `- Journal matches:  _SYSTEMD_UNIT=ssh.service + _COMM=sshd
`- Actions
   |- Currently banned: 3
   |- Total banned:     27
   `- Banned IP list:   203.0.113.5 198.51.100.7 192.0.2.44
```

## 7. Ruční zásahy

```bash
sudo fail2ban-client set sshd banip 203.0.113.5        # ručně zabanovat
sudo fail2ban-client set sshd unbanip 203.0.113.5      # odbanovat jednu IP
sudo fail2ban-client unban 203.0.113.5                 # odbanovat ve všech jailech
sudo fail2ban-client unban --all                       # odbanovat všechno
sudo fail2ban-client set sshd addignoreip 192.168.1.50 # přidat výjimku za běhu (do restartu)
```

## 8. Ladění a vlastní filtry

```bash
# Otestuje filtr proti logovému souboru (kolik řádků by zachytil)
sudo fail2ban-regex /var/log/auth.log /etc/fail2ban/filter.d/sshd.conf

# Test proti systemd journalu
sudo fail2ban-regex systemd-journal /etc/fail2ban/filter.d/sshd.conf
```

- Hotové filtry: `/etc/fail2ban/filter.d/`
- Hotové akce: `/etc/fail2ban/action.d/`
- Další jail (např. pro nginx): v `jail.local` přidejte sekci
  `[nginx-http-auth]` s `enabled = true` (a případně `logpath`).

## 9. Rychlé řešení problémů

- **Jail se nespustí:** zkontrolujte `sudo journalctl -u fail2ban -n 50`
  a `sudo fail2ban-client -t`. Nejčastěji chybí logový soubor
  (`logpath`), balíček `python3-systemd`, nebo je v konfiguraci překlep.
- **Nic se nebanuje:** odpovídá `port`, `backend` a `logpath`? Vyzkoušejte
  `fail2ban-regex` proti reálnému logu.
- **Zamkl jsem se:** z konzole serveru (panel VPS) spusťte
  `sudo fail2ban-client unban <moje IP>` a přidejte IP do `ignoreip`.
- **Používáte UFW:** fail2ban ve výchozím stavu přidává vlastní pravidla
  `f2b-*` do iptables/nftables a funguje souběžně s UFW. Případně
  nastavte `banaction = ufw`.
- **Po upgradu Ubuntu** zkontrolujte, že `jail.local` stále odpovídá
  (backend, cesty k logům).

## 10. Minimální postup od nuly

1. `sudo apt install fail2ban python3-systemd`
2. Vytvořit `/etc/fail2ban/jail.local` (viz výše), nastavit `ignoreip`,
   `bantime`, `maxretry` a sekci `[sshd]`.
3. `sudo fail2ban-client -t`
4. `sudo systemctl enable --now fail2ban` (nebo `restart`)
5. `sudo fail2ban-client status sshd`

## Další zdroje

* Projekt a dokumentace: <https://github.com/fail2ban/fail2ban>
* Manuálové stránky: `man jail.conf`, `man fail2ban-client`, `man fail2ban-regex`
* Související návod: [SSH – správa klíčů a připojení](/navody/ssh)
