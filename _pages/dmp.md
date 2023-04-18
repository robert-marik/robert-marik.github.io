---
title: Dynamické modely populací
author: Robert Mařík
date: 2023-02-10
category: Jekyll
layout: post
---

> ##### Upozornění, aktuality
>
> * Dne 2.3.2023 byl zpřesněn postup odevzdávání seminární práce. Součástí bude zapracování drobných připomínek přímo v učebně. Více viz níže.
{: .block-danger }



{% include float_image.html image_path="/images/dmp_logo.jpg" description='Liška ostrovní. Příklad živočišného druhu, který se podařilo zachránit před vyhynutím [v rekordně krátkém čase](https://www.nature.org/en-us/about-us/where-we-work/united-states/california/stories-in-california/endangered-island-foxes-break-record-for-fast-recovery/"), během dekády. K tomu byla nutná komplexní znalost ekosystému a analýza, jak se projeví jednotlivé zásahy do vztahů v tomto ekosystému. Zdroj: commons.wikimedia.org.' %}



## Rozcestník předmětu

-   Učební text je primárně v [online
    formě](https://robert-marik.github.io/dmp). K dispozici je i verze v
    [PDF](https://user.mendelu.cz/marik/dmp/Dynamicke_modely_populaci_text.pdf).
    V současnosti (leden 2023) v textu chybí závěrečné kapitoly, ty
    budou doplněny během semestru.
-   [JupyterHub server na MENDELU](https://jupyter.mendelu.cz)

## Požadavky na ukončení

  * Odevzdání **seminární práce** a zapracování případných připomínek.  
  * **Docházka** do cvičení a na přednášky nebo **zápočtová písemka**.

Pro _presenční formu_ se za splnění docházky považují nejvýše tři absence na přednášce a nejvýše tři absence ve cvičení. Absence nemusí být omluvené ani nemusí být podložené neschopenkou.

Pro _kombinovanou formu_ se za splnění docházky považuje jedna neúčast. Absence nemusí být omluvené ani nemusí být podložené neschopenkou.

Pro obě formy může být zápočtová písemka nahrazena ústním pohovorem, ve kterém student prokáže, že má přehled o studované problematice.

Detaily k zápočtové písemce budou zveřejněny během semestru. Zjednodušeně, půjde o nějakou modifikaci některého z modelů studovaných v předmětu, při které student ukáže, že si osvojil hlavní myšlenky a postupy používané při formulaci a studiu těchto modelů. Případně detailní vysvětlení některých aspektů některého z probíraných modelů.


#### Seminární práce

-   Dokument v Jupyter notebooku obsahující textový popis vybraného
    modelu (vhodný model z literatury či internetu včetně plné citace
    nebo vhodná modifikace modelu z přednášky), numerickou simulaci
    (například vliv počátečních podmínek nebo vliv parametrů) s
    grafickým výstupem a slovní interpretaci výsledku.
-   Dokument bude obsahovat základní formátování: Nadpis, jméno autora,
    datum, odrážky, matematické výrazy ve formátu LaTeX.
-   Vhodným modelem se rozumí například mírná modifikace něčeho, co jsme
    studovali na přednášce. Modifikace by měla být netriviální, ale není
    nutné se pouštět do komplikovaných věcí. V případě potřeby můžete se
    mnou nejprve nápad prodebatovat. Pokud se Vám nebude dařit vhodný
    model ke studiu najít, kontaktujte mne a já vám něco doporučím.
-   **Ukázka seminární práce** je na JupterHub serveru ve sdíleném
    adresáři `my_shared_folder` pod názvem
    `seminarni_prace_marik.ipynb`. Je nasdílena i [zde](https://gist.github.com/robert-marik/5f16044072d78c730ee13d58bcd24ff9). Na konci obsahuje vhodné nápady pro téma seminární práce. 
-   Kdo si není jistý formou nebo rozsahem seminární práce, může ji
    nejprve probrat s vyučujícím.
-   Dokument musí být uložen ve Vašem hlavním adresáři na serveru
    jupyter.mendelu.cz. Název dokumentu bude
    `seminarni_prace_login.ipynb` kde místo `login` bude Váš login,
    například `seminarni_prace_marik.ipynb`. Kromě toho uložíte
    identický ipynb soubor do odevzdávárny v UIS.
-   Vložení souboru do odevzdávárny v UIS slouží pro oficiální záznam o
    odevzdání a jako signál toho, že se mám podívat na Váš soubor na
    JupyterHub serveru. Do tohoto souboru případně vepíšu komentáře a
    požadavky na úpravu a přes odevzdávárnu dostanete zprávu, je-li vše
    OK, nebo jestli je potřeba něco upravit.
-   > **Aktualizace 2.3.2023** Výše popsaným postupem budou řešeny     zásadnější a závažné připomínky k práci. Plně uznána bude práce po     zapracování drobnějších připomínek přímo v učebně. Termíny budou     vypsány v UIS, přihlašování bude jako na klasické zkoušky nebo    zápočty.
    {: .block-warning }
-   > **Návrh na seminární práci 1** Některá modifikace Levinsova modelu metapopulací, návrhy jsou na konci [cvičení](https://robert-marik.github.io/dmp/cviceni/cviceni_08.html).
-   > **Návrh na seminární práci 2** Model [konkurence tří druhů](https://robert-marik.github.io/dmp/prednaska/09.html#model-konkurence-tri-druhu) je možno snadno přeměnit na model konkurence dvou druhů majících společného predátora. Například změnou třetí rovnice na 
    >
    >$$\frac{\mathrm dz}{\mathrm dt}=(-m+px+qy)z$$ 
	>
    > bychom dostali model dravce a kořisti s konkurencí mezi populacemi kořisti a predátorem Lotkova--Volterrova typu. Ukažte, že dravec může být činitelem, který jedné z populací může zprostředkovat přežití. Ukažte, že v případě, kdy je konkurence taková, že jeden druh dominuje a druhý vymírá, může přítomnost predátora dominanci zastavit a tím zprostředkovat přežití jeho kořisti. Najděte tedy nastavení parametrů tak, aby simulace, které se liší jenom počáteční hodnotou predátora (jednou nula a jednou nenulová hodnota) vypadaly například tak jako na následujícím obrázku. Tato simulace podporuje názor, že pestřejší společenstva jsou stabilnější, protože po odstranění dravce by zůstal jenom jediný druh. ![](/images/korist-korist-dravec.png){:class="img-responsive"}

## Presenční forma, harmonogram semestru

> -   Přednášky čtvrtek 11:00–13:00, učebna B44
> -   Cvičení úterý 13:00–14:00 a 14:00–15:00, učebna B514
> -   Cvičení je před přednáškou a až na několik výjimek se vztahuje k
>     náplni přednášky z týdne předcházejícího cvičení.

<!-- -->

* 1\. týden semestru (týden od 13.2.2023)
  * Cvičení: [Úvod do
        předmětu](https://robert-marik.github.io/dmp/intro.html) a
        [první kroky v
        Pythonu](https://robert-marik.github.io/dmp/Prvni_kroky.html)
  * Přednáška: [Funkce a vlastnosti
        funkcí](https://robert-marik.github.io/dmp/prednaska/01.html)
  * [Video ke cvičení](https://youtu.be/9TORLQb0m-E)
* 2\. týden semestru (týden od 20.2.2023)
  * Cvičení: [Úvod do jazyka Python](https://robert-marik.github.io/dmp/cviceni/cviceni_01.html)
  * Přednáška: [Derivace a integrál](https://robert-marik.github.io/dmp/prednaska/02.html)
  * [Video o práci se soubory](https://youtu.be/-Uq0pUT-n1U)
  * [Video o tvorbě tabulky s daty a vykreslení těchto dat](https://youtu.be/tY23bobO3wA) a [výsledný zápisník](https://gist.github.com/robert-marik/d089a26d1b55f1afa3613c887fad4ad1)
* 3\. týden semestru (týden od 27.2.2023)
  * Cvičení: [Úvod do řešení rovnic s derivacemi](https://robert-marik.github.io/dmp/cviceni/cviceni_02.html)
  * Přednáška: [Diferenciální rovnice](https://robert-marik.github.io/dmp/prednaska/03.html)
  * [Rychlý přehled ovládání Jupyter notebooku](https://robert-marik.github.io/ntb)
* 4\. týden semestru (týden od 6.3.2023)
  * Cvičení: [Diferenciální rovnice 1](https://robert-marik.github.io/dmp/cviceni/cviceni_03.html)
  * Přednáška: [Autonomní diferenciální rovnice](https://robert-marik.github.io/dmp/prednaska/04.html)
  * [Video o řešení diferenciálních rovnic](https://youtu.be/h-D7D3smZlA) a [výsledný zápisník](https://gist.github.com/robert-marik/f47aebec85b4dd650e5a108a881606be)
* 5\. týden semestru (týden od 13.3.2023)
  * Cvičení: [Diferenciální rovnice 2](https://robert-marik.github.io/dmp/cviceni/cviceni_04.html)
  * Přednáška: [Bifurkace](https://robert-marik.github.io/dmp/prednaska/05.html)
* 6\. týden semestru (týden od 20.3.2023)
  * Cvičení: [Diferenciální rovnice 3](https://robert-marik.github.io/dmp/cviceni/cviceni_05.html)
  * Přednáška: [Maticové modely](https://robert-marik.github.io/dmp/prednaska/06.html)
* 7\. týden semestru (týden od 27.3.2023)
  * Cvičení: [LaTeX](https://robert-marik.github.io/dmp/cviceni/cviceni_06.html)
  * Přednáška: [Parciální derivace](https://robert-marik.github.io/dmp/prednaska/07.html)
* 8\. týden semestru (týden od 3.4.2023)
  * Cvičení: [Maticové modely](https://robert-marik.github.io/dmp/cviceni/cviceni_07.html)
  * Přednáška: [Autonomní systémy](https://robert-marik.github.io/dmp/prednaska/08.html)
* 9\. týden semestru (týden od 10.4.2023)
  * Cvičení: [Metapopulace](https://robert-marik.github.io/dmp/cviceni/cviceni_08.html)
  * Přednáška: [Modely konkurence populací](https://robert-marik.github.io/dmp/prednaska/09.html)
  * [Video o řešení rovnice metepopulací pro různé parametry](https://youtu.be/83h1C4Bq2GI) a [výsledný zápisník](https://gist.github.com/robert-marik/e8f6f0d555d06bfe0009d9665870f38a)
* 10\. týden semestru (týden od 17.4.2023)
  * Cvičení: [Konkurence](https://robert-marik.github.io/dmp/cviceni/cviceni_09.html). Je k dispozici [zápisník](https://gist.github.com/robert-marik/ac2d0f53d3013c031914948fc824890d) a [první](https://user.mendelu.cz/marik/temp/dmp/nb_diff1.html) a [druhý](https://user.mendelu.cz/marik/temp/dmp/nb_diff2.html) diff. Zápisník [po první úpravě](https://gist.github.com/robert-marik/a03721940147b618802dd69d60a52c64) a [po druhé úpravě](https://gist.github.com/robert-marik/d809801ec278c6254ff90b3255c6a976).
  * Přednáška: [Modely dravce a kořisti](https://robert-marik.github.io/dmp/prednaska/10.html)
* 11\. týden semestru (týden od 24.4.2023)
* 12\. týden semestru (týden od 1.5.2023) Výuka se nekoná, hlavní cvičení.
* 13\. týden semestru (týden od 8.5.2023) Výuka se nekoná, hlavní cvičení.
* 14\. týden semestru (týden od 15.5.2023)

## Kombinovaná forma, harmonogram semestru

Materiály viz [Dynamické modely
populací](https://robert-marik.github.io/dmp/intro.html)

-   Čtvrtek 9.2.2023 9:00–13:00 B514 (4 hodiny) Přednášky 1 až 3,
    cvičení 1 až 4.
-   Pátek 10.2.2023 13:00–16:00 B46 (3 hodiny) Přednášky 4 a 5, cvičení
    5, 6, 9.
-   Pátek 17.3.2023 13:00–16:00 B514 (3 hodiny) Dokončení z minula. Dle možností přednášky 6 a 7, cvičení
    7 a 8
-   Pátek 31.3.2023 13:00–16:00 B514 (3 hodiny) Přednášky 8, 9, 10, 11,
    cvičení 10 a 11
-   Pátek 12.5.2023 16:00–19:00 B514 (3 hodiny) Přednáška 12 cvičení 12

## Požadované dovednosti 

> ##### Upozornění
>
>Následující seznam obsahuje požadované dovednosti, které budou náplní zápočtové písemky anebo součástí požadavků na finální úpravu seminární práce. 
>
>Seznam bude doplňován vždy po probrání látky na presenčním studiu.
{: .block-danger }

### Požadované dovednosti pro zápočtovou písemku

* Schopnost vysvětlit, jakou roli hraje při formulaci modelů derivace. Jaká je slovní interpretace derivace, jaká je její fyzikální jednotka.
* Vysvětlit rovnici ochlazování. Podat slovní interpretaci jednotlivých částí rovnice a vysvětlit, proč jsou sestaveny právě užívaným způsobem.
* Vysvětlit jednotlivé stavební složky rovnice dynamické rovnováhy počtu druhů na ostrovech (McArthur, Wilson) a jejich závislost na velikosti ostrova resp. vzdálenosti od pevniny. Vysvětlit chování řešení a změnu polohy stacionárních bodů v závislosti na parametrech. 
* Vysvětlit podstatu základních populačních modelů, model exponenciálního růstu (Malthusův) a logistického růstu (Verhulstův). Modelování populace v prostředí s omezenou nosnou kapacitou.
* Vliv lovu na dynamiku populace v prostředí s omezenou nosnou kapacitou, různé strategie lovu, stabilita stacionárních bodů. Modelování Alleeho efektu.
* Vysvětlit podstatu modelování populace s věkovou strukturou, Leslieho a Lefkovitchovy matice. 
* Markovovy řetězce, modelování vývoje lesa z hlediska druhového složení.
* Maticové modely, dynamika růstu (dominantní vlastní hodnota, příslušný vlastní vektor) a vliv parametrů na tuto dynamiku, matice elasticity, reprodukční hodnota jednotlivých věkových kategorií.
* Parciální derivace a jejich využití k lineární aproximaci. Rovnice difuze pro modelování šíření invazního druhu.

### Požadované dovednosti pro finální úpravu seminární práce

Z následujícího seznamu se použije to, co je relevantní pro danou práci. Například u práce věnované maticovým modelům se nebude vyžadovat nic co by se týkalo pouze diferenciálních rovnic a naopak.

* Nakreslení funkce, nastavení popisků os a rozsahů na osách. Nadpis grafu. Legenda v případě více křivek.
* Sestavení tabulky po sloupcích a vykreslení křivek definovaných daty ve sloupcích.
* Vyřešení diferenciální rovnice a vizualizace řešení. Pro jednu nebo více počátečních podmínek. Zapsání dat do tabulky.
* Vyřešení diferenciální rovnice a vizualizace řešení pro několik hodnot parametrů. Zapsání dat do tabulky. 
* Schopnost zapsat běžné matematické výrazy v systému $\LaTeX$. Schopnost napsat bez typografických chyb text, obsahující matematické vzorce a matematické výrazy.


## Literatura

Viz [sylabus](https://is.mendelu.cz/katalog/syllabus.pl?predmet=140853)
v Univerzitním informačním systému. Naprostá většina materiálů (Tkadlec,
Dykyjová, Begon) je dostupná v knihovně nebo studovně MENDELU. Jedná se
o klasická díla v ekologii. Murray je ze sítě MENDELU k dispozici
online.

### Online literatura

-   J. D. Murray, [Mathematical
    biology](https://link.springer.com/book/10.1007/b98868)
-   J. R. Chasnov, [Lecture Notes on Mathematical
    Biology](https://www.math.hkust.edu.hk/~machas/mathematical-biology.pdf)
-   [Virtual Ecology
    Portal](http://ecovirtual.ib.usp.br/doku.php?id=en:ecovirt:start)
    (tutoriály a numerické simulace pro základní ekologické modely)
-   L. Edelstein-Keshet [Open Calculus
    Book](https://personal.math.ubc.ca/~keshet/keshet.html) (spíše
    matematika)
-   G. A. Enciso [Youtube videa Mathematical
    biology](https://www.youtube.com/playlist?list=PLqOZ6FD_RQ7lnGZ7fkn503y_7U4rrJ-Se)

Přístup k literatuře může být omezen a literatura nemusí být přístupná
ze sítě mimo MENDELU. V takovém případě použijte
[proxy](http://proxy.mendelu.cz).

### Další zdroje informací

Matematiky moc používat nebudeme, naprostá většina věcí okolo modelů je krásně vysvětlena v publikaci prof. Tkadlece, úzkým hrdlem budou proto asi IT skills.

* Nejlepší tutoriál Pythonu na světě je <https://www.w3schools.com/python/>. Obsahuje i matplotlib, NumPy, Pandas. 
* Pro LaTeX stačí umět psát základní matematické výrazy. Pomůže například [nápověda pro Wikpedii](https://cs.wikipedia.org/wiki/N%C3%A1pov%C4%9Bda:Matematick%C3%A9_vzorce), která používá stejný mechanismus. Případně [tento přehled](https://user.mendelu.cz/marik/am/slidy/latex/).
* Nejlepší servery, kam se chodí pro rady ohledně rozbitého a nefungujícího kódu a pro rady jak něco udělat v Pythonu nebo LaTeXu, jsou <https://stackoverflow.com/questions/tagged/python> a <https://stackexchange.com>. Můžete například kopírovat chybové hlášky do Google vyhledávače a preferovat odkazy směřující na tyto servery.
