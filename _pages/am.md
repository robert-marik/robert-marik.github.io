---
title: Aplikovaná/Inženýrská matematika
author: Robert Mařík
date: 2023-02-05
category: Jekyll
layout: post
---

{% include float_image.html image_path="/images/am_logo.jpg" description='Pro popis vlastností v materiálu je zásadní schopnost modelovat transport tekutin a energie materiálem. Na obrázku výzkumá aparatura VCJR v Útěchově.' %}

### Úvodem

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

Předmět je postaven jako navazující kurz, odpovídá obvyklé navazující
matematice na technických školách příbuzných LDF. Zohledňuje však
zaměření školy a požadavky na absolventy, kteří budou ze získaných
znalostí těžit v 21. století, ve století kdy výpočetní výkon letí
nahoru a v mobilu má každý jedinec vyšší výpočetní výkon, než počítače
použité k prvnímu letu na Měsíc. Tato skutečnost ovlivňuje i konkrétní
náplň předmětu.

Do předmětu jsou zařazeny partie týkající se diferenciálního a integrálního
počtu funkcí více proměnných a vektorových funkcí a dále kapitoly z
diferenciálních rovnic. Důraz je více než na počítání konkrétních
derivací nebo integrálů kladen na představení souvislostí a nastínění
spektra aplikací tohoto aparátu. Tím se předmět liší od obecně pojatých
matematik, které jsou nejčastější a je k nim nejvíce literatury. Jinak
řečeno, nebude pro nás stěžejní to, jak se vypočítá parciální derivace,
ale jak tuto derivaci můžeme použít k popisu dějů a jevů ve dřevě, v
materiálech obecně, nebo v přírodě okolo nás.

Předmět navazuje na znalosti matematiky získané v bakalářském stupni
studia. Měli byste znát derivace, integrály a operace s maticemi
(definice a využití). Měli byste umět derivovat a integrovat polynomy,
počítat determinanty třetího řádu. Tyto znalosti je možné načerpat
nebo si zopakovat [zde](https://robert-marik.github.io/pages/mt/).


## Informace


* Texty přednášek a cvičení jsou dostupné na [GitHub Pages, Aplikovaná
  matematika](https://robert-marik.github.io/am/).
* Presenční studium: podmínky pro ukončení, ukázkové písemky, přihlašování do
  domácích úloh jsou k dispozici v [Moodle Mendelu, Aplikovaná
  matematika](https://moodle.mendelu.cz/course/view.php?id=814). Při
  přihlašování do Moodle použijte Shibboleth login a stejné údaje jako při
  přihlašování do UIS. Pro zápis do předmětu použijte kód, který bude rozeslán
  mailem na začátku výuky a sdělen na přednášce. Můžete si ho i zjistit od
  spolužáků. 
* Kombinované studium: podmínky pro ukončení, ukázkové písemky, login a heslo pro
  přihlašování do
  domácích úloh sdělí vyučující. 


## Přednášky a cvičení

Rozpis témat je orientační a bude přizpůsobován podle běhu semestru. Aktuální informace budou v Moodle.


{::options parse_block_html="true" /}

<div class="predmet">

### Diferenciální operátory

1. ![01.jpg](/images/am/01.jpg) *Při
studiu přírody nás přirozeně zajímají změny veličin, protože jsou hybnou
silou nebo kvantitativním popisem veškerého dění. Seznámíme se s
parciálními derivacemi, které dokáží zachytit rychlost změn, ať už v
čase, nebo v prostoru nebo v abstraktním prostoru. Toto je možno využít
ke kvantitativnímu popisu přírodních dějů. Jako aplikaci parciálních
derivací odvodíme rovnici vedení tepla v jedné dimenzi. Tu je možno
použít například při modelování prostupu tepla stěnou nebo oknem.*
     * [AI videopodcast](https://youtu.be/ZxaLsLVz51Q)
     * [Přednáška](https://robert-marik.github.io/am/01)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni01.html)
1. ![02.jpg](/images/am/02.jpg) *Gradient
je diferenciální operátor sestavený z parciálních derivací tak, aby
odkryl další přírodní zákony. Zejména tok. Gradient umožní popsat
skutečnost, že mnoho přírodních dějů vede k tomu, že se příroda snaží
nastolit rovnováhu. Proudění se tedy děje z míst, kde je něčeho více.
Přesně tento směr dokáže podchytit pojem gradient. K tomuto se ještě
přidává fakt, že příroda někdy usměrňuje proudění v materiálech do svých
preferovaných směrů. Jsou to jakési dálnice, které strhávají například
proudění hmoty nebo tepla. Ve dřevu jsou tyto dálnice poměrně výrazné a
jsou v podélném směru.*
     * [AI videopodcast](https://youtu.be/AO_GZ8J4PwE)
     * [Přednáška](https://robert-marik.github.io/am/02)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni02.html)
1. ![03.jpg](/images/am/03.jpg) *Podrobněji se podíváme
na proudění a sestavíme matematický model tak obecného proudění, že jím
pokryjeme přenos látky i přenos energie. Jako aplikaci ukážeme
matematický popis libovolného transportního jevu. Toto zahrnuje jako
speciální případy vedení tepla, proudění mělké nebo podzemní vody,
difuzi nebo sušení dřeva. Častým praktickým úkolem je modelování
fyzikálních polí (teploty a vlhkosti) v okolí okna.*
     * [Přednáška](https://robert-marik.github.io/am/03)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni03.html)
     * [Je náš svět 3D?](https://user.mendelu.cz/marik/am/slovni_ulohy/#parci%C3%A1ln%C3%AD-derivace-vektorov%C3%A9ho-pole)
1. ![04.jpg](/images/am/04.jpg) *Seznámíme
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
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni04.html)

### Integrály funkce více proměnných

1. ![05.jpg](/images/am/05.jpg) *Rozšíříme
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
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni05.html)
1. ![06.jpg](/images/am/06.jpg) *Pokračujeme v rozšiřování integračních možností a naučíme se integrovat přes dvourozměrné množiny. Aplikací je například výpočet charakteristik důležitých pro posouzení odolnosti nosníku vůči
deformaci. Jinou aplikací výpočet tlaku na plochu ponořenou napříč
různými hloubkami.*
     * [Přednáška](https://robert-marik.github.io/am/06)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni06.html)
1. ![07.jpg](/images/am/07.jpg) *Poznáme
obecné věty, které dávají fyzikální význam operátorům rotace a
divergence. Umožňují převod mezi lokálním a globálním tvarem fyzikálních
zákonů a dávají konečně odpověď na otázku, ke kterým vektorovým polím je
možno zavést skalární potenciál a jak. Vedlejším produktem je vysvětlení
funkce planimetru nebo výpočet křivkového integrálu druhého druhu pomocí
kmenové funkce.*
     * [Přednáška](https://robert-marik.github.io/am/07)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni07.html)

### Diferenciální rovnice

1. ![08.jpg](/images/am/08.jpg) *Seznámíme
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
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni08.html)
1. ![09.jpg](/images/am/09.jpg) *Linearita.
Důležitá vlastnost, která usnadňuje řešení matematických modelů. Modely,
které jsou lineární se chovají v jistém smyslu pěkně a mnoho vlastností
mají podobných. Naprostá většina technicky zajímavých jevů a dějů snese
lineární aproximaci a tím pádem umožní i jednotný popis řešení tak, jak
se s ním seznámíme na přednášce.*
     * [Přednáška](https://robert-marik.github.io/am/09)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni09.html)
1. ![10.jpg](/images/am/10.jpg) *Poznáme
speciální soustavy diferenciálních rovnic, které jsou nezávislé na čase
a umožňují modelování interagujících populací (různé druhy konkurence,
modely dravce a kořisti apod). Ukážeme si model vývoje vzorců chování a
vysvětlení principu přemnožení lesního škůdce. Dalšími aplikacemi jsou
kompartmentové modely, které popisují jakési přelévání veličin, které
modelujeme, mezi různými stavy. Využití je od chemických reakcí přes
model složeného žaludku nebo šíření epidemie až k modelu odtoku srážek z
regionu.*
     * [Přednáška](https://robert-marik.github.io/am/10)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni10.html)
1. ![11.jpg](/images/am/11.jpg) *V této
přednášce se seznámíme s lineárními diferenciálními rovnicemi druhého
řádu. Těmito rovnicemi je prostoupena v podstatě celá klasická
mechanika. Mají uplatnění při studiu kmitavých pohybů strun, desek nebo
těles. Dále při studiu nosníků namáhaných na vzpěr a v úlohách
založených na třech Newtonových pohybových zákonech. Naučíme se metody
řešení, ale zaměříme se i na to, jakým způsobem se obyčejná lineární
diferenciální rovnice druhého řádu objeví při studiu parciálních
diferenciálních rovnic, například při studiu rovnice vedení tepla.*
     * [Přednáška](https://robert-marik.github.io/am/11)
     * [Cvičení](https://robert-marik.github.io/am/cviceni/cviceni11.html)
1. Základní postupy numerické matematiky. Diskretizace a nondimenzionalizace diferenciálních rovnic. Numerické řešení.
     * [Konečné diference](https://robert-marik.github.io/am/01/#numericka-aproximace-derivaci-konecne-diference)
	     * [Konečné diference a řešení DR Eulerovou metodou](https://user.mendelu.cz/marik/manim/Diference/)
	 * [Nondimenzionalizace](https://robert-marik.github.io/am/08/#transformace-diferencialni-rovnice) obyčejné diferenciální rovnice
	     * [Nondimenzionalizace v růstových modelech](https://robert-marik.github.io/am/10/#logisticka-diferencialni-rovnice-s-predatory)
	 * [Nondimenzionalizace](https://robert-marik.github.io/matematika/numerika/index.html#nondimenzionalizace-a-bezrozmerne-veliciny) parciální diferenciální rovnice
	     * [Vajont, šílenství mužů](https://www.youtube.com/watch?v=H3IwAdrCdgQ&t=3612s)
	     * [Tsunami v horách](https://www.youtube.com/watch?v=BK5uwnVCeCw&t=2185s)
		 * [Differential analyzer z Merkuru](https://www.youtube.com/watch?v=LqTL2JBETzE)
		 * [Differential analyzer ve filmu](https://www.youtube.com/watch?v=TQj3PsSDoUo)
	 

</div>


