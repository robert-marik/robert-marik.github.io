---
title: Jupyter Notebook
author: Robert Mařík
date: 2012-12-15
layout: post
permalink: ntb
lightbox: true
---

{::options parse_block_html="true" /}

<style>
.prispevky img {float:right; max-width:400px !important; padding-left:10px;}

h2 {clear:both;}

.markdown-section code {border-style:solid; border-color:black; border-width:1px; margin:2px !important; padding:1px; clear:both;}
</style>


<div class="prispevky">

Se zápisníky Jupyter máte po ruce to nejlepší pro zpracování a
manipulaci s daty, co může současný stav informačních technologií
nabídnout.

* Python je výkonný nástroj pro práci s daty a řešení numerických úloh.
* Jupyter notebook umožní používat Python v prohlížeči, aniž byste cokoliv instalovali. Práce je podobná běžné práci s informačními systémy, server obstarává výpočty, prohlížeč odesílá příkazy a zobrazuje výsledky výpočtů. 
* Jupyter notebook je ideální pro kombinaci zpracování dat a popisu, jaké techniky byly použity. Je to ideální laboratorní deník pro práci s daty.
* Python a Jupyter mají podporu velkých firem. Například Facebook a Google. Důkazem je alternativní prostředí pro výpočty <https://colab.research.google.com/>, možnost sdílení zápisníků na <https://github.com/> a <https://gist.github.com/>. Nebo knihovna pro predikci vývoje časových řad [Prophet](https://facebook.github.io/prophet/)

{% include lightbox.html file="jupyter_main.png" %}

Ovládání zápisníku Jupyter je intuitivní a rychle se s ním každý sžije. Níže je několik nejdůležitějších pokynů.

* Pro orientaci v prostředí si můžete spustit Help -> User Interface Tour (cca 2 minuty)
* Seznam klávesových zkratek je k dispozici v menu Help -> Keyboard Shortcuts
* V naprosté většině případů (kromě psaní textu s diakritikou) je lepší mít přepnuto na anglickou klávesnici.

## Práce se soubory


{% include lightbox.html file="jupyter_download.png" %}

* Přejmenování souboru je možné kliknutím na název zápisníku (je součásti User Interface Tour). Další možnosti jsou v menu (uložit pod jiným názvem, uložení s časovou značkou, vytvoření kopie, vytvoření nového zápisníku)
* Na svůj lokální počítač můžete zápisník stáhnout pomocí File -> Download as -> Notebook (ipynb). Další volby (PDF, html) nemusí fungovat, pokud nejsou na server nainstalovány příslušné balíčky. Html soubor se dá vytvořit i pomocí File -> Print preview.

## Práce s buňkami (textovými i příkazovými)

{% include lightbox.html file="jupyter_run.png" %}

Do zápisníku můžeme vkládat nové buňky, měnit textové buňky na příkazové a naopak, můžeme buňky kopírovat, vkládat, vystřihávat, mazat. Vše se dá naklikat v menu, ale klávesové zkratky jsou pohodlnější a rychlejší.

* `A` vloží buňku nad (Above) aktivní buňku
* `B` **vloží buňku pod (Below) aktivní buňku**
* `C` kopíruje aktivní buňku
* `X` vystřihne aktivní buňku
* `V` vloží zkopírovanou nebo vystřihnutou buňku pod aktivní buňku
* `Shift+V` vloží zkopírovanou nebo vystřihnutou buňku nad aktivní buňku
* `M` **mění aktivní buňku na textovou (Markdown)**
* `Y` **mění aktivní buňku na příkazovou**
* `Z` je Undo k vymazání buňky
* `D` `D` **maže aktivní buňku (dvakrát stisknout D)**
* šipky nahoru a dolů způsobí pohyb po buňkách, se Shiftem rozšiřují výběr.
* `Shift+M` **spojí vybrané buňky (pokud jsou vybrané) anebo připojí následující buňku (je-li vybraná jenom jedna)**
* `F` spustí vyhledávání nebo Najdi/Nahraď. Je možné používat regulární výrazy. Vyhledávání se omezí na aktivní nebo označené buňky.

Přesun buněk nahoru/dolů je jenom v menu, ale je pro něj ikona v toolbaru anebo se dá rychle realizovat vystřižením a vložením pod, tj. stiskem `X`, `V`.


## Editace příkazových buněk

* šipky nahoru a dolů způsobí pohyb po řádcích, se Shiftem rozšiřují výběr.
* výběr, posun po slovech, kopírovaní, vystřihování a vkládání obvyklými zkratkami (Shift+šipka, Ctrl+ šipka, Ctrl+C, Ctrl+X, Ctrl+V)
* `Ctrl+/` zapoznámkovává nebo ruší zapoznámkování označených řádků.
* `Tab` **odsadí řádek nebo blok, zvětší odsazení o 4 mezery**
* `Tab` **za rozepsaným jménem funkce nebo proměnné nabídne doplnění**
* `Shift+Tab` **zmenší odsazení o 4 mezery**
* `Shift+Tab` za jménem funkce vyvolá nápovědu
* `Ctrl+Z` je Undo pro editaci. Funguje pro každou buňku samostatně.
* `Ctrl+Y` nebo `Shift+Ctrl+Z` je Redo pro editaci.
* `Ctrl+Shift+-` **rozdělí buňku na řádku s kurzorem** (nejprve `Crtl` a potom `Shift` a `-`, jinak ve většině prohlížečů zmenšuje písmo)
* `Esc` ukončí editaci
* `Ctrl+Enter` **spustí buňku**
* `Shift+Enter` **spustí buňku a přemístí se na následující. Pokud je buňka na konci, vloží se další**
* `Alt+Enter` spustí buňku, pod ni vloží novou buňku a přesune se na novou buňku


## Editace textových buněk

Stejné jako s programovým kódem, jenom například doplňování proměnných a příkazů zde nedává smysl. Napravo je náhled při editaci. Matematické výrazy se zapisují pomocí LaTeXu.

## Další tipy 

{% include lightbox.html file="jupyter_control_panel.png" %}

* Do hlavního adresáře se dostanete kliknutím na ikonu jupterhub vlevo nahoře. Zde jsou i po označení souborů nástroje na kopírování, přejmenování, editaci atd.
* Pokud spotřebujete veškeré prostředky, které máte přiděleny, můžete po kliknutí na Control Panel vpravo nahoře zastavit a znovu spustit server, který Vás obsluhuje.

</div>
