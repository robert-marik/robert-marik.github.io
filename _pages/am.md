---
title: Aplikovaná matematika
author: Robert Mařík
date: 2023-02-05
category: Jekyll
layout: predmet
---


{% include float_image.html image_path="/images/am_logo.jpg" description='Pro popis vlastností v materiálu je zásadní schopnost modelovat transport tekutin a energie materiálem. Na obrázku výzkumá aparatura VCJR v Útěchově.' %}


Letní semestr - jaro 2022/2023

## Úvodem

Předmět se drží těchto zásad:

-   **Matematika není počítání příkladů.** Počítání příkladů se sice nejlépe
    učí a nejlépe zkouší, ale to není důvod odhlédnout od toho
    nejdůležitějšího, k čemu to vlastně je.
-   **Pozitivní motivace funguje lépe než hrozby.** Nemusíte chodit do
    výuky, nemusíte odevzdávat domácí úkoly. Ale pokud budete,
    proplujete předmětem výrazně snadněji.
-   Každý nepotřebuje být skvělý modelář a výpočtář. Ale každému se
    hodí mít **co nejširší spektrum znalostí.** Základní znalosti o
    metodách, pomocí kterých modelujeme svět je užitečné každému, kdo
    chce být odborníkem. Dá to například představu o limitech a
    možnostech využití výpočtů a modelů.

Kurz je postaven jako navazující kurz, odpovídá obvyklému druhému kurzu
matematiky na technických školách příbuzných LDF. Zohledňuje však
specifika školy a požadavky na absolventy, kteří budou ze znalostí
získaných v kurzu těžit v 21. století, ve století kdy výpočetní výkon
letí nahoru a v mobilu má každý jedinec vyšší výpočetní výkon, než
počítače použité k prvnímu letu na Měsíc. Tato skutečnost ovlivňuje i
konkrétní náplň předmětu.

Do kurzu jsou zařazeny partie týkající se diferenciálního a integrálního
počtu funkcí více proměnných a vektorových funkcí a dále kapitoly z
diferenciálních rovnic. Důraz je více než na počítání konkrétních
derivací nebo integrálů kladen na představení souvislostí a nastínění
spektra aplikací tohoto aparátu. Tím se kurz liší od obecně pojatých
kurzů, které jsou nejčastější a je k nim nejvíce literatury. Jinak
řečeno, nebude pro nás stěžejní to, jak se vypočítá parciální derivace,
ale jak tuto derivaci můžeme použít k popisu dějů a jevů ve dřevě, v
materiálech obecně, nebo v přírodě okolo nás.

## Rozcestník elektronických informačních zdrojů

Následující nástroje jsou kriticky důležité pro studium.

* Webová stránka, kterou právě čtete. Veřejně
přístupné informace dlouhodobějšího charakteru.
* WeBWorK je primární nástroj pro kontrolu a evidenci práce během
semestru, odevzdávání domácích úkolů. Tato činnost je dobrovolná a má
nemalý vliv na závěrečné hodnocení (viz podmínky ukončení).
  * [presenční forma](https://um.mendelu.cz/webwork2/AM_2023_pres/)
  * [kombinovaná forma](https://um.mendelu.cz/webwork2/AM_2023_komb/)
* [UIS](https://is.mendelu.cz), univerzitní informační systém použijeme pro hromadné maily od učitele, přihlašování na zápočty a zkoušky, distribuci hesel pro WeBWorK.


## Základní materiály

> Materiály jsou k dispozici z minulých semestrů a mohou být a budou mírně
> upravovány, aby reflektovaly aktuální situaci
>
> * [Materiály k přednáškám](https://robert-marik.github.io/am) jsou k dispozici jako texty
> s vloženými odkazy na Youtube mikropřednášky.
> * [Materiály pro cvičení](https://robert-marik.github.io/am/cviceni/cviceni00.md.html) jsou k dispozici v podobné formě jako pro
> přednášky.
> * [Cheatsheet](https://raw.githubusercontent.com/robert-marik/apl-slidy/master/cheatsheet/cheatsheet-AM.pdf) pro Aplikovanou matematiku. Vzorce, důležitá fakta.
> * Cheatsheet pro [věci související s IT](https://raw.githubusercontent.com/robert-marik/hw-webwork/master/cheatsheet/cheatsheet.pdf): WeBWorK a LaTeX. Základní příkazy.
{: .block-warning }


> -   Cvičení i domácí úkoly bývají tematicky k přednášce ze stejného
>     týdne.
> -   Domácí úloha se pro presenční studenty zpravidla otevírá v den, kdy
>     se látka z této úlohy probírá na přednášce a je na ni minimálně
>     týden.
{: .block-tip }



## Přednášky presenční, LS 2022-2023 (jaro 2023)



-   Rozpis je orientační a bude přizpůsobován podle běhu semestru.
    Podobně se může posouvat otevírání a uzavírání domácích úloh.


<!-- 
Délka videí vložených do přednášek: Do textů přednášky a cvičení jsou vložena videa jako mikropřednášky. To šetří čas (poslechnu jenom to, kde problematice nerozumím ze čteného textu) i orientaci (nemusí se hledat v hodinovém a delším videu). Přibližná doba videí (čas trvání zaokrouhelný na celé minuty a posčítaný pro přednášku i cvičení) je následující.
```
Údaje k 1.3.2021
Týden 01, prednaska + cviceni 01: 140 minut
Týden 02, prednaska + cviceni 02: 151 minut
Týden 03, prednaska + cviceni 03: 81 minut
Týden 04, prednaska + cviceni 04: 84 minut
Týden 05, prednaska + cviceni 05: 107 minut
Týden 06, prednaska + cviceni 06: 104 minut
Týden 07, prednaska + cviceni 07: 74 minut
Týden 08, Prednaska + cviceni 08: 100 minut
Týden 19, Prednaska + cviceni 09: 103 minut
Týden 10, prednaska + cviceni 10: 80 minut
Týden 11, prednaska + cviceni 11: v priprave
``` 
-->

Data v harmonogramu odpovídají úterní přednášce. Cvičení je o den
později ve středu.

1. ![00.jpg](/images/am/00.jpg) *Základy matematické gramotnosti. Práce
se systémem WeBWorK.* Vyzkoušejte si systém pro domácí úlohy.
     *  [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/00_Uvod/) 
1. 14.02.2023 ![01.jpg](/imageshttps://robert-marik.github.io/am/01.jpg) *Při
studiu přírody nás přirozeně zajímají změny veličin, protože jsou hybnou
silou nebo kvantitativním popisem veškerého dění. Seznámíme se s
parciálními derivacemi, které dokáží zachytit rychlost změn, ať už v
čase, nebo v prostoru nebo v abstraktním prostoru. Toto je možno využít
ke kvantitativnímu popisu přírodních dějů. Jako aplikaci parciálních
derivací odvodíme rovnici vedení tepla v jedné dimenzi. Tu je možno
použít například při modelování prostupu tepla stěnou nebo oknem.*
     * [Přednáška](https://robert-marik.github.io/am/01)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni01.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/01_Parcialni_derivace)
1. 21.2.2023 ![02.jpg](/imageshttps://robert-marik.github.io/am/02.jpg) *Gradient
je diferenciální operátor sestavený z parciálních derivací tak, aby
odkryl další přírodní zákony. Zejména tok. Gradient umožní popsat
skutečnost, že mnoho přírodních dějů vede k tomu, že se příroda snaží
nastolit rovnováhu. Proudění se tedy děje z míst, kde je něčeho více.
Přesně tento směr dokáže podchytit pojem gradient. K tomuto se ještě
přidává fakt, že příroda někdy usměrňuje proudění v materiálech do svých
preferovaných směrů. Jsou to jakési dálnice, které strhávají například
proudění hmoty nebo tepla. Ve dřevu jsou tyto dálnice poměrně výrazné a
jsou v podélném směru.*
     * [Přednáška](https://robert-marik.github.io/am/02)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni02.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/02_Gradient)
1. 28.2.2023 Koná se jenom cvičení ve středu. Typografické konvence v
matematice a v textech obsahujících matematiku. (V úterý je hlavní
cvičení na oboru TMZD.) 
1. 7.3.2023 ![03.jpg](/imageshttps://robert-marik.github.io/am/03.jpg) *Podrobněji se podíváme
na proudění a sestavíme matematický model tak obecného proudění, že jím
pokryjeme přenos látky i přenos energie. Jako aplikaci ukážeme
matematický popis libovolného transportního jevu. Toto zahrnuje jako
speciální případy vedení tepla, proudění mělké nebo podzemní vody,
difuzi nebo sušení dřeva. Častým praktickým úkolem je modelování
fyzikálních polí (teploty a vlhkosti) v okolí okna.*
     * [Přednáška](https://robert-marik.github.io/am/03)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni03.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/03_Divergence)
1. 14.3.2023 ![04.jpg](/imageshttps://robert-marik.github.io/am/04.jpg) *Seznámíme
se s dalším vektorovým operátorem. Ten nám umožní rozhodnout, zda je
proudění nebo silové pole popsatelné skalární veličinou. To souvisí s
možností či nemožností zavést ve studovaném poli potenciální energii a
je to tedy otázka možnosti či nemožnosti razantně zjednodušit modelování
procesů v takovém poli. Jako vedlejší produkt poznáme kritérium které
rozhodne, zda pole roztáčí objekty, které jsou tímto polem unášeny.
Takové je třeba rychlostní pole v řece. Praktické využití znají
například vodáci, kteří najíždí do proudu napříč a proud je sám stočí
obloučkem do svého směru.*
     * [Přednáška](https://robert-marik.github.io/am/04)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni04.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/04_Rotace)
1. 21.3.2023 ![05.jpg](/imageshttps://robert-marik.github.io/am/05.jpg) *Rozšíříme
si výpočet integrálu o možnost integrovat podle libovolné křivky. Tím je
možno počítat napětí v cylindrických nádobách pod tlakem a zjistit, proč
trubky praskají podélně. Jinou aplikací je možnost definovat potenciál i
v abstraktních případech nesouvisejících s mechanickou prací. Známý je
například vodní potenciál při studiu evapotranspirace stromů nebo
rostlin. Práce souvisí s potenciální energií a proto se dá čekat, že
bude i souvislost s operátorem rotace, představeným na předchozí
přednášce. Na takovou souvislost si ovšem budeme muset ještě nějaký ten
týden počkat.*
     * [Přednáška](https://robert-marik.github.io/am/05)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni05.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/05_Krivkovy_integral)
1. 28.3.2023 ![06.jpg](/imageshttps://robert-marik.github.io/am/06.jpg) *Pokračujeme v rozšiřování integračních možností a naučíme se integrovat přes dvourozměrné množiny. Aplikací je například výpočet charakteristik důležitých pro posouzení odolnosti nosníku vůči
deformaci. Jinou aplikací výpočet tlaku na plochu ponořenou napříč
různými hloubkami.*
     * [Přednáška](/imageshttps://robert-marik.github.io/am/06)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni06.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/06_Dvojny_integral)
1. 4.4.2021 ![07.jpg](/imageshttps://robert-marik.github.io/am/07.jpg) *Poznáme
obecné věty, které dávají fyzikální význam operátorům rotace a
divergence. Umožňují převod mezi lokálním a globálním tvarem fyzikálních
zákonů a dávají konečně odpověď na otázku, ke kterým vektorovým polím je
možno zavést skalární potenciál a jak. Vedlejším produktem je vysvětlení
funkce planimetru nebo výpočet křivkového integrálu druhého druhu pomocí
kmenové funkce.*
     * [Přednáška](https://robert-marik.github.io/am/07)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni07.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/07_Integraly_souhrn)
1. 11.4.2021 ![08.jpg](/imageshttps://robert-marik.github.io/am/08.jpg) *Seznámíme
se s přirozeným nástrojem pro formulaci fyzikálních zákonů a přírodních
dějů obecně: s diferenciálními rovnicemi. Fyzika střední školy obsahuje
zpravidla jenom děje probíhající za speciálních podmínek. V reálu nás v
přírodě zajímají změny a souvislosti změn s ostatními veličinami. Tyto
změny se vyjadřují pomocí derivací a souvislosti poté pomocí
diferenciálních rovnic. Diferenciální rovnice jsou takto ideálním
prostředkem pro popis přírodních zákonů. Typickým představitelem je
radioaktivní rozpad (a s ním související například ochrana budov) nebo
tepelná výměna. Další aplikace jsou v modelování populací živočišných a
rostlinných druhů v různých podmínkách.* Obrázek z <https://www.hauff-technik.de/en/company/industry-news/radon-safe-construction>
.
     * [Přednáška](https://robert-marik.github.io/am/08)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni08.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/08_Diferencialni_rovnice)
1. 18.4.2021 ![09.jpg](/imageshttps://robert-marik.github.io/am/09.jpg) *Linearita.
Důležitá vlastnost, která usnadňuje řešení matematických modelů. Modely,
které jsou lineární se chovají v jistém smyslu pěkně a mnoho vlastností
mají podobných. Naprostá většina technicky zajímavých jevů a dějů snese
lineární aproximaci a tím pádem umožní i jednotný popis řešení tak, jak
se s ním seznámíme na přednášce.*
     * [Přednáška](https://robert-marik.github.io/am/09)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni09.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/09_Autonomni_systemy) Domácí úkol je vztahuje i k následujícímu týdnu.
1. 25.4.2023 ![10.jpg](/imageshttps://robert-marik.github.io/am/10.jpg) *Poznáme
speciální soustavy diferenciálních rovnic, které jsou nezávislé na čase
a umožňují modelování interagujících populací (různé druhy konkurence,
modely dravce a kořisti apod). Ukážeme si model vývoje vzorců chování a
vysvětlení principu přemnožení lesního škůdce. Dalšími aplikacemi jsou
kompartmentové modely, které popisují jakési přelévání veličin, které
modelujeme, mezi různými stavy. Využití je od chemických reakcí přes
model složeného žaludku nebo šíření epidemie až k modelu odtoku srážek z
regionu.*
     * [Přednáška](https://robert-marik.github.io/am/10)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni10.md.html)
     * [Domácí úkol](https://um.mendelu.cz/webwork2/AM_2023_pres/10_Shrnuti) Domácí úkol se nevztahuje k látce tohoto týdne, ale jedná se o shrnutí celého semestru.
1. 2.5.2023 ![11.jpg](/imageshttps://robert-marik.github.io/am/11.jpg) *V této
přednášce se seznámíme s lineárními diferenciálními rovnicemi druhého
řádu. Těmito rovnicemi je prostoupena v podstatě celá klasická
mechanika. Mají uplatnění při studiu kmitavých pohybů strun, desek nebo
těles. Dále při studiu nosníků namáhaných na vzpěr a v úlohách
založených na třech Newtonových pohybových zákonech. Naučíme se metody
řešení, ale zaměříme se i na to, jakým způsobem se obyčejná lineární
diferenciální rovnice druhého řádu objeví při studiu parciálních
diferenciálních rovnic, například při studiu rovnice vedení tepla.*
     * [Přednáška](https://robert-marik.github.io/am/11)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni11.md.html)
1. 9.5.2023 Bude doplněno. Základní postupy numerické matematiky.
Diskretizace a nondimenzionalizace diferenicálních rovnic. 
1. 16.5.2023 Bude doplněno. Závěrečné shrnutí.



<!--

1. 10.5. a 11.5. 2022 Opakování, poznámky k numerické matematice, Python.
   * [První kroky](https://gist.github.com/robert-marik/a3b7b095cbb625433e4f223c782ea6d4)
   * [Obrázky](https://gist.github.com/robert-marik/39326af3283d42d405b37315a460dfcf)
   * [Grafy](https://gist.github.com/robert-marik/fbdb71509f336d0c6b0162aa80a4f0f8)
   * [Tabulky](https://gist.github.com/robert-marik/d4abaf37237dfd8214b71b860ac601f4)
   * [Krabicové grafy, Anova](https://gist.github.com/robert-marik/635affe37158d3fae1ef4f5bf3798dd8)
   * [Worksheet, kombinace textu a výpočtů](https://gist.github.com/robert-marik/a545aa84f0ec91ab3fe62611835ee300)
   * [Definice funkcí](https://gist.github.com/robert-marik/d6477e04195410a830535addd502a4db)
   * [Cykly, citlivostní analýza](https://gist.github.com/robert-marik/6b2667e26c09d1b047efab66ace3a58d)
   * [Autonomní systém](https://gist.github.com/robert-marik/faec576e20ca03398960437ad6a81e75)
   * [Numerické experimenty](https://gist.github.com/robert-marik/6ccefd5d473a49ee8597d9df4409ddc9)
   * [Numerické experimenty s libovolnou přesností](https://gist.github.com/robert-marik/7eb864d3bc5d995772164baf13299e79)
   * [Tabulka, regrese](https://gist.github.com/robert-marik/83ce4b15af7df4b54e3aa639ba5461d6)
   * [Tabulka, predikce budoucnosti](https://gist.github.com/robert-marik/3dcc8c5bc635f24913d3de0fa35426dd)
1. 17.5. a 18.5. 2022 Rezerva, opakování, shrnutí
   * [Staré písemky](http://user.mendelu.cz/marik/am/pisemky/zadani.pdf)
   * [Volgograd (kmity mostu)](https://www.youtube.com/watch?v=ZjazqDW8zLI)

-->

## Informace k ukončení

> #### Obsah a forma zkouškové písemky
> -   Maximální zohlednění toho, co se dělalo ve cvičeních na přednáškách
>     a v domácích úlohách. Učte se podle materiálů pro daný semestr,
>     nikoliv podle starých písemek, které již nemusí stoprocentně
>     reflektovat přednášenou náplň.
> -   Cca polovina teorie a polovina počítání, ale často se to prolíná.
> -   Důraz bude na difuzní rovnici (co znamenají jednotlivé členy, jak se
>     liší v různých situacích), diferenciální rovnice (sestav podle
>     slovního popisu modelu), parciální derivace ve všech variantách
>     (gradient-divergence-rotace, jednotka, slovní význam), křivkový
>     integrál druhého druhu (z definice nebo pomocí skalárního
>     potenciálu). Písemka z roku 2022 je na adrese
>     <http://user.mendelu.cz/marik/am/pisemky/pisemky_2022/> jako vzor.
{: .block-tip }


Písemka je "openbook". Během písemky je možné pracovat s vlastní
literaturou na fyzickém nosiči. **Mezi literaturu se nepočítá přístup na
internet ani programy na matematické výpočty.** Povolené jsou knihy,
vytištěné materiály k našemu předmětu (přednášky, cvičení, domácí úkoly)
nebo jakékoliv další texty, vlastní rukopisné poznámky, okopírované
jakékoliv papíry, ... Literatura nesmí být na elektronickém nosiči
(notebook, tablet, mobil, čtečka, hodinky, mp3 přehrávač, ...).

Ústní část zkoušky se plánuje jako doplněk k písemce pouze na případnou
žádost studenta. 

> #### Podmínky na ukončení
>
> -   Součet bodů za písemku a bonusových bodů (viz domácí úkoly a
>     docházka níže) a musí být **alespoň 25 bodů.** To odpovídá
>     úspěšnosti 50 procent při nevyužití bonusových bodů za práci během
>     semestru sledovanou pomocí domácích úkolů a docházky. To také
>     odpovídá snížení laťky pro písemku u studentů, prokazatelně
>     aktivních během semestru.
> -   Současně písemka **alespoň na 13 bodů z 50**.
> -   **Hodnocení.** Podle součtu bodů z písemky, domácích úloh a za
>     docházku. A (56-70 bodů), B (48-55 bodů), C (41-47 bodů), D (33-40
>     bodů), E (25-32 bodů), F (nevyhověl).
> -   Rychlé ústní ověření znalostí v případě, kdy o ústní zkoušení požádá
>     student, nebo kdy nastanou nějaké nejasnosti ohledně vypracovaných
>     úkolů.
{: .block-tip }

> #### Domácí úkoly
>
> Během semestru budou
> zadávány dobrovolné domácí úlohy v systému
> [WeBWorK](https://um.mendelu.cz/webwork2/AM_2023_pres). Tyto domácí
> úlohy se budou započítávat ke zkoušce. Bez jejich plnění je nutné mít u
> zkoušky polovinu bodu. Při plnění domácích úkolů je možné tuto laťku
> snížit, jak je popsáno v následujících odstavcích.
>
> **Bonus za domácí úkoly je nejvýše 20 bodů.** Bonusy jsou přidělovány
> následovně (součet za všechny úlohy je 160 bodů)
>
> * 20 bonusových bodů za hodnocení alespoň 90% bodů z domácích úloh, tj. alespoň 144 bodů,
> * 15 bonusových bodů za alespoň 70% bodů z domácích úloh, tj. alespoň 112 bodů,
> * 10 bonusových bodů za alespoň 60% bodů z domácích úloh, tj. alespoň 96 bodů, 
> * 6 bonusových bodů za alespoň 50% bodů z domácích úloh, tj. alespoň 80 bodů.
> * 4 bonusové body za alespoň 33% bodů z domácích úloh, tj. alespoň 53 bodů.
{: .block-warning }

> #### Docházka
> Docházka není povinná, ale
> minimalizování počtu absencí je vnímáno jako aktivita v semestru a
> připočteno k dobru u zkoušky.
>
> **Bonus za docházku** je nejvýše 5 bodů.
>
> * Za nejvýše tři absence na přednášce 3 bonusové body. Za 4 absence jsou 2 bonusové body, za 5 absencí jeden bonusový bod, za více absencí nic. 
> * Za nejvýše tři absence na cvičení 2 bonusové body. Za 4 absence jeden bonusový bod, za více absencí nic.
{: .block-warning }

**Staré písemky** jsou k dispozici. (Pozor na to, že předmět se vyvíjel
a například před pěti lety vypadala přednášená látka a i závěrečná
písemka jinak.)

* [zde](https://user.mendelu.cz/marik/am/pisemky/) pro Aplikovanou
matematiku 
* [zde](https://user.mendelu.cz/marik/pisemky/inzenyrska_matematika/)
pro Inženýrskou matematiku. 
* Staré písemky a jejich řešení nejsou
zamýšleny jako studijní literatura. Řešení jsou načmrknutá v ruce a
slouží pro orientaci, kterým směrem se odpověď má ubírat. Jsou užitečné
jako nápověda a orientační bod pro člověka, který o problematice něco
ví. Jako primární studijní materiál nebo jako literatura používaná během
písemky jsou staré písemky bezcenné a spíše přítěží. 
* Postupem času
oba předměty Aplikovaná matematika a Inženýrská matematika
dokonvergovaly do jednoho, takže to je jedno. Dříve však byla náplň
poněkud odlišná, proto se dívejte na to, zda jsou typy příkladů pro daný
běh relevantní. (Například tam, kde je v těchto písemkách úloha na
řešení lineární diferenciální rovnice druhého řádu, bude nahrazena něčím
jiným. To proto, že od COVIDu19 ruční řešení diferenciální rovnice
druhého řádu do výuky nezařazujeme, ale soustředíme se na užitečnější
věci.)


## Několik zásad a tipů na hladké proplutí předmětem

##### Matematika není počítání.

Nepoužíváme paradigma, že matematika jsou příklady a jejich počítání.
Toto paradigma je sice zažité, protože příklady se dobře učí a snadno
zkouší ve všech fázích vzdělávání, ale falešné a patří do minulého
století. Proto jsou **příklady pouze malou částí zkoušky**. Jsou
jednoduché, protože spíše než získávat rutinu na počítání by si na nich
studenti měli osahat pojmy zmiňované na přednáškách a uvědomit postupy a
souvislosti.

##### Literatura u zkoušky není všespasitelná.

Literatura u zkoušky pomůže jenom tomu, kdo se v problematice orientuje,
má **základní znalosti v hlavě** a je schopen si dohledat detaily v
litartuře a porozumět jim.

##### Jako vážně domácí úkoly?

Zkouška je složitelná po splnění běžných požadavků (polovina bodů ze
zkouškové písemky) i bez jakékoliv aktivity během semestru. Zkušenosti
však ukazují, že pracovat během semestru a **získávat bonusové body se
velmi vyplácí**, zejména studentům, kteří takzvaně "nemají buňky na
matematiku".

##### Samostudium je normální.

Opustíme obvyklé schema, kdy učitel odprezentuje veškerou náplň
přednášky, ale po půl hodině bohužel zůstává v obraze jenom malé
procento posluchačů. **Na přednášce se vysvětlí základní principy** a
předpokládá se, že studenti se seznámí se zbytkem přednbášky
individuálním čtením.

##### Videa opravdu nejsou to pravé.

Je málo nudnějších věcí než youtube přednáška nebo počítání příkladů z
matematiky. Stejné informace získáte čtením textu mnohem rychleji.
Neexistuje zdlouhavější činnost, než vyhledávání informace ve videu.
Text prohledáte mnohem rychleji. Nehledejte kouzelná videa, která vám
znalosti "nalijí do hlavy". **Snažte se pracovat s textem.** Videa a
videopřednášky použijte až jako poslední záchranu. Jsou skvělé pokud
absolutně tápete., Ale i v takovém případě se snažte postupně přecházet
od sledování videí k práci s textem a případně využijte konzultace nebo
se ptejte v hodině.


## Další odkazy

Následující nástroje mohou být vaši pomocníci

-   Kurz navazuje na znalosti matematiky získané v bakalářském stupni
    studia. Měli byste znát derivace, integrály a operace s maticemi
    (definice a využití). Měli byste umět derivovat a integrovat
    polynomy, počítat determinanty třetího řádu. Tyto znalosti je možné
    načerpat nebo si zopakovat [zde](https:/user.mendelu.cz/marik/mt).


