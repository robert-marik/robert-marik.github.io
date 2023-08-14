---
title: Python
author: Robert Mařík
date: 2000-02-15
layout: post
permalink: python
---

<div style="float:right; width:600px; max-width:50%; clear:both; padding:10px;">
<img src="/images/posts/python.png" style="max-width:100%;" >
</div>

Tato stránka je určena pro začátečníky v Pythonu. Používá se například v
předmětu Úvod do systémové biologie.

#### Proč Python?

Python je někdy považován za programovací jazyk pro neprogramátory.
Jedná se o jeden z nejvhodnějších nástrojů na analýzu dat, simulace,
výpočty a vizualizace. Jaké jsou jeho důležité vlastnosti?

-   Je neinteraktivní. Autor zadá své představy a spustí výpočet.
    Výpočet proběhne automaticky. Výhodou oproti interaktivní práci
    nabízené některými softwarovými nástroji je transparentnost výpočtu.
    I zpětně je jasné, co se ve kterém okamžiku počítalo. Další výhodou
    je, že je možné úlohu spouštět automatizovaně nebo v cyklu nad
    různými sadami vstupních dat. Obrovskou nevýhodou je mnohem delší
    zaškolení na práci se systémem v porovnání s programy s grafickým
    uživatelským prostředím. Pro vážnou práci však tuto nevýhodu
    přebíjejí pozitivní faktory.
-   Je moderní. Proto je investice vložená do učení se jazyka Python
    investicí do budoucna. V tomto jazyce pracují velké firmy (Google,
    Facebook), jsou k dispozici moderní nástroje (strojové učení,
    predikce časových řad).
-   Je široce rozšířený. Python je jeden z nejpoužívanějších
    programovacích jazyků na světě. Pokud máte v Pythonu s něčím
    problém, pravděpodobně měl stejný problém i někdo jiný, řešil tento
    problém v diskusních fórech na internetu a řešení je dohledatelné v
    příslušných diskusních fórech na Internetu. Například [dotaz na
    spojování
    seznamů](https://stackoverflow.com/questions/1720421/how-do-i-concatenate-two-lists-in-python).
    Je i řada blogových zápisků věnovaných různým problematikám,
    například [A Guide to Time Series Forecasting in
    Python](https://builtin.com/data-science/time-series-forecasting-python)
-   Je snadno dostupný a free. Proto můžete Python používat bez
    počáteční investice, ať již finanční (nákup programu) nebo časové
    (instalace systému).
-   Je srozumitelný. Většina jeho programových konstrukcí je čitelnější
    a bližší přirozenému jazyku, než ekvivalenty v jiných jazycích pro
    numerické simulace (Matlab, Octave).
-   Python obsahuje knihovny. Nemusíte integrovat ručně, nemusíte ručně
    řešit diferenciální rovnice. Vše důležité a používané je k dispozici
    ve formě připravených knihoven. Programátor v podstatě skládá
    skládačku z modulů a funkcí, které připravili experti. Je zvykem si
    funkce knihoven osahat na jednoduchých úlohách, kdy výstup je možné
    potvrdit i ručním výpočtem a ujistit se, že kód počítá to, co
    opravdu chceme. Proto nějaké drobné počítání je součástí práce
    výpočtáře, většinou se však jedná o jednoduché úlohy.

#### Práce v Pythonu

Python je interpretovaný jazyk. Výsledkem je skript (sada instrukcí),
nikoliv samostatně spustitelný program. Proto je potřeba s ním pracovat
v nějakém vývojovém prostředí pro pořizování, spouštění a ladění
programového kódu.

Jsou dvě základní varianty. Buď výpočty běží v cloudu a Váš počítač
jenom zprostředkovává komunikaci přes Internet, nebo výpočty běží na
vašem lokálním PC.

-   V cloudu. Nemusíte nic instalovat. Jste však závislí na výpočetním
    výkonu, který poskytovatel služby nechává uživatelům těchto služeb.
    Pokud pracujete anonymně a nemáte v cloudu úložiště, musíte práci
    stáhnout na lokální PC (a optimálně stahovat i během práce)
    -   [JupyterHub na MENDELU](https://jupyter.mendelu.cz) bude
        pracovní prostředí pro studenty předmětu [Dynamické modely
        populací](/pages/dmp).
    -   [Google Colab](https://colab.research.google.com) umožňuje
        pracovat s Pythonem v prostředí zápisníku Jupyter. Vyžaduje
        registraci u Googlu. Data se ukládají na Google Drive a je možné
        je sdílet buď na Drive nebo na
        [GitHubu](https://gist.github.com/robert-marik/7eb864d3bc5d995772164baf13299e79).
        Pro běžnou práci nezahrnující mnohahodinové simulace je
        dostačující. Je možné ukládat různé verze dokumentu a v případě
        potřeby se k nim vracet.
    -   [Try Jupyter](https://jupyter.org/try) je stránka, na které si
        můžete spustit vlastní Jupyter notebook pro práci v Pythonu (a
        mnohem více) bez jakékoliv aktivace účtu. Po ukončení práce si
        stáhněte soubor na lokální PC.
    -   [7 ways to run Jupyter Notebook
        online](https://mljar.com/blog/jupyter-notebook-online/),
        Aleksandra Płońska a Piotr Płoński
-   Na lokálním PC. Musíte si vše nainstalovat na svůj počítač, ale
    nejste závislí na výkonu poskytnutého zprostředkovatelem služby ani
    na Internetovém připojení.
    -   [Anaconda](https://www.anaconda.com/products/distribution)
        obsahuje Jupyter notebook pro zápisníky kombinující text s
        programovým kódem a editor Spyder pro psaní a ladění programů v
        Pythonu. Toto je nainstalováno v učebně B46. Je to
        nejpohodlnější cesta jak nainstalovat Python a nejčastěji
        používané nástroje pro práci v Pythonu.
    -   [Instalace
        Pythonu](https://naucse.python.cz/lessons/beginners/install/),
        pokud nepotřebujete instalovat celou Anacondu. Měli byste si
        také nainstalovat nějaký editor usnadňující práci nebo nějaké
        IDE (Visual Studio, Spyder, \...).

#### Návody pro Python

##### Návody pro Python jako programovací jazyk

Kdo má zkušenosti s programováním, stačí mu seznámit se se základní
syntaxí a případné věci si dohledat za pochodu nebo okoukat na
příkladech. Pro ostatní jsou plnohodnotné kurzy.

-   [Python Tutorial na w3schools](https://www.w3schools.com/python/) je
    kurz na W3schools, největší autorita na poli vyučování IT
    technologií
-   [Nauč se Python!](https://naucse.python.cz/course/pyladies/), kurz v
    češtině

##### Návody pro knihovny používané v Pythonu

-   [Knihovna NumPy](https://numpy.org/), práce s daty, numerická
    matematika
-   [Knihovna SciPy](https://scipy.org/), některé další algoritmy
    numerické matematiky
-   [Knihovna matoplotlib](https://matplotlib.org/), grafy a grafický
    výstup dat
-   [Knihovna pandas](https://pandas.pydata.org/), analýza dat, práce s
    daty v tabulkách, vizualizace dat

##### Návody pro Jupyter

Návody pro Jupyter (prostředí oblíbené pro psaní a spouštění příkazů
Pythonu) nejsou v podstatě potřeba. Stačí pár klávesových zkratek
(seznam dostupný přes menu v položce Help) a vše je intuitivní. Pokud by
se však někdo chtěl rozkoukat\...

-   [Introduction to Jupyter
    Notebooks](https://www.section.io/engineering-education/introduction-to-jupyter-notebooks/)
    by Adith Bharadwaj
-   [Jupyter Notebook: An
    Introduction](https://realpython.com/jupyter-notebook-introduction/)
-   [Quick introduction to Jupyter
    Notebook](https://www.youtube.com/watch?v=jZ952vChhuI) - videoukázka
-   [Get started with Google Colaboratory (Coding
    TensorFlow)](https://www.youtube.com/watch?v=inN8seMm7UI) -
    videoukázka práce v Colab, Google variantě Jupyteru
