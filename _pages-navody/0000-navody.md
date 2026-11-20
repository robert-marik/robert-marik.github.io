---
title: Návody a taháky – rozcestník
author: Robert Mařík
date: 2026-11-20
layout: post
permalink: navody
---

Stručné praktické návody a taháky k nástrojům, které používám při práci
s počítačem, serverem a Pythonem. Každý návod je samostatný a dá se číst
jako referenční přehled příkazů s vysvětlením.

## Přehled návodů

* [Git – tahák](/navody/git) – základní příkazy, větve, diff, porovnání
  lokálního repozitáře se serverem, historie po merge a vracení změn.
* [SSH – správa klíčů a připojení](/navody/ssh) – generování klíčů,
  konfigurace klienta, `ssh-agent`, zabezpečení serveru, omezení klíčů
  v `authorized_keys` a řešení častých chyb.
* [fail2ban na Ubuntu](/navody/fail2ban) – instalace, konfigurace jailů,
  kontrola funkčnosti, přehled zabanovaných adres a ladění filtrů.
* [uv – správce Pythonu a projektů](/navody/uv) – verze Pythonu,
  projekty, závislosti, lock soubor, skripty, nástroje, publikace balíčků,
  Docker a CI.
* [Python v Dockeru s micromambou](/navody/docker-micromamba) – vývojové
  prostředí v kontejneru s kódem a daty na lokálním disku, napojení
  editoru a výkon na Linuxu.

## Poznámka ke vzniku

Návody vznikly s pomocí umělé inteligence (Claude), byly zkontrolovány
a upraveny. Nástroje se vyvíjejí, proto si příkazy před použitím na
produkčním systému ověřte v dokumentaci nebo pomocí `--help` a `man`.

Související stránky: [Příkazy pro Linux](/bash), [Python](/python).
