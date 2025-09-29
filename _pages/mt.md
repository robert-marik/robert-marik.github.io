---
title: Matematika
author: Robert Mařík
date: 2023-02-01
category: Jekyll
layout: post
---

{% include float_image.html image_path="/images/mtk_logo.jpg" description='V 21. století má každý nástroje pro simulace na dosah ruky. I pojetí matematiky je proto vhodné posunout od "jak vypočítat jednoduchý příklad" k "jak naformulovat a zadat užitečný model". Na obrázku je měření teplotního toku dřevěným panelem ve VCJR v Útěchově. Popis transportu energie a hmoty bude jeden z našich hlavních cílů.' %}

Předmět odpovídá obecným úvodům do matematiky na technicky zaměřených
oborech s jednosemestrální výukou matematiky. Obsahuje diferenciální a
integrální počet a lineární algebru. Je však pojetím a skladbou
příkladů silně zaměřen na praktické využití matematiky ve vědách o
přírodě a přírodních materiálech. Toto pojetí zahrnuje dřevo
(dřevařství, arboristika, nábytek, dřevostavby), půdu (krajinářství) i
ekosystémy (lesnictví).

Například **derivaci** poznáme jako nástroj pro
detekci **prostorové nebo časové změny veličiny**. Nikoliv jako směrnici
tečny z obecně zaměřených učebnic nebo Wikipedie.

**Integrál** poznáme především jako cestu od **rychlosti změny k velikosti** této změny. Nikoliv jako
obsah obrazce. To je sice obvyklá představa, ale v materiálovém
inženýrství málo užitečná.

**Lineární algebru** nezaměříme na soustavy
lineárních rovnic, které za nás dnes řeší počítače tak, že vše vlastně
probíhá na pozadí a my o tom ani nevíme. Zaměříme se raději na využití
vyjadřovacích prostředků lineární algebry **v popisu materiálů**, které
mají význačné směry ve kterých se liší jejich fyzikální
vlastnosti. Dřevo totiž mezi takové materiály bezesporu patří.

Jak plyne z předešlých odstavců, předmět se malinko liší od obecně
zaměřených matematických přednášek. Ke zvládnutí čistě matematického
aparátu existuje v online i tištěné podobě nepřeberné množství snadno
dostupného materiálu. Všechno potřebovat nebudeme. Ale budeme
potřebovat poznatky, které se z takové záplavy informací těžko
vyzobávají a v těch ryze matematicky orientovaných materiálech ani
nejsou. Proto je silně doporučeno sledovat náplň kurzu a přizpůsobit
tomu práci během semestru a výběr literatury. To poněkud zvyšuje
nároky na studenty, ale je nutné si uvědomit, že cílem předmětu není
přispět k výchově poloprofesionálních matematiků, jak tomu může být na
obecně zaměřených oborech. Chceme otevřít dveře poznání studentům,
kteří mají ambice studovat přírodu a prostředí okolo nás prostředky
dostupnými v 21. století.


## Informace

Veškeré informace kromě přednášek a cvičení jsou k dispozici v [Moodle Mendelu, Matematika MTK](https://moodle.mendelu.cz/course/view.php?id=968). Při přihlašování do Moodle použijte Shibboleth login a stejné údaje jako při přihlašování do UIS. Pro zápis do předmětu použijte kód, který bude rozeslán mailem na začátku výuky a sdělen na přednášce. Pozor: bude se lišit pro presenční a kombinovanou formu studia.


## Přednášky a cvičení

Předmět je rozdělen na 12 přednášek, k přednáškám, jsou cvičení, která dle rozvrhu a státních svátků mohou nabrat až několikatýdení zpoždění.

{::options parse_block_html="true" /}

<div class="predmet">

### Derivace

1. ![01.jpg](/images/mtk/01.jpg)
*Přednáška o derivacích, základním stavebním kamenu pro studium funkcí.
Naučíme se matematicky popsat rychlost. Ve cvičení se naučíme derivovat
a tuto znalost využijeme v týdnech bezprostředně následujících. Naučíme
se například pro veličiny spojené fyzikálním vzorcem najít souvislost
mezi rychlostmi změn těchto veličin. Jedna z aplikací je měření odporu
dřeva pro stanovení vlhkosti.*

     * [Přednáška 1](https://robert-marik.github.io/matematika/derivace_I) (Derivace funkce)
     * [Cvičení 0](https://robert-marik.github.io/matematika/cviceni/cviceni00.html) (Úvod)
     * [Cvičení 1](https://robert-marik.github.io/matematika/cviceni/cviceni01.html) (Základy derivací)
     * [Cvičení 2](https://robert-marik.github.io/matematika/cviceni/cviceni02.html) (Využití derivací v matematických modelech)

1. ![02.jpg](/images/mtk/02.jpg)
*Naučíme se využít derivace k rozumné aproximaci funkcí a fyzikálních
zákonů. Tím se mnoho vztahů stane významně jednoduššími a matematické
modely se stanou spočitatelnými i bez superpočítačů. Ukážeme si dále
polynomiální aproximaci, která umožní zachytit jevy z podstaty
nelineární, jako je například laser. Ale rozebereme si i řešitelnost
rovnic a možnosti jejich numerického řešení.*

     * [Přednáška 2](https://robert-marik.github.io/matematika/derivace_II) (Derivace a lineární aproximace)
     * [Cvičení 3](https://robert-marik.github.io/matematika/cviceni/cviceni03.html) (Výpočet derivací, lineární aproximace)

1. ![03.jpg](/images/mtk/03.jpg)
*Další využití derivací, tentokrát zaměřeno na extrémy. Naučíme se
hledat optimální stavy systému. Například jak vyřezat co nejtužší nosník z kulatiny (musím řezat
obdélníkový profil). Seznámíme se s pojmem gradient, který dokáže
identifikovat směr podnětů dávajících do pohybu vedení tepla nebo
transport látek. A poprvé se seznámíme s bezrozměrnými veličinami, které
přijdou ke slovu i později.*

     * [Přednáška 3](https://robert-marik.github.io/matematika/derivace_III) (Derivace a další užitečné nástroje)
     * [Cvičení 4](https://robert-marik.github.io/matematika/cviceni/cviceni04.html) (Lokální extrémy)

### Integrál

1. ![04.jpg](/images/mtk/04.jpg)
*Derivaci jsme poznali jako míru měřící rychlost změn a nyní si uvedeme
opačnou úlohu. Znalost rychlosti s jakou se mění nějaká veličina nám
umožní najít tuto veličinu. Naučíme se například najít změnu teploty u
procesu, u kterého intenzita tepelné výměny klesá s časem.*

     * [Přednáška 4](https://robert-marik.github.io/matematika/integraly) (Integrál, integrál a integrál)
     * [Cvičení 5](https://robert-marik.github.io/matematika/cviceni/cviceni05.html) (Integrály I)

1. ![05.jpg](/images/mtk/05.jpg)
*Integrály pro pokročilé. Naučíme se numericky aproximovat určitý
integrál a dokonce otevřeme vrátka mimo svět elementárních funkcí.*

     * [Přednáška 5](https://robert-marik.github.io/matematika/integraly2) (Integrály pro pokročilé)
     * [Cvičení 6](https://robert-marik.github.io/matematika/cviceni/cviceni06.html) (Integrály II)

### Diferenciální rovnice

1. ![06.jpg](/images/mtk/06.jpg)
*Fyzikální zákony formulujeme pomocí rychlostí změn (derivací) a
důsledky hledáme řešením vzniklých rovnic, zpravidla vhodným
integrováním. Problematika spadá do oblasti diferenciálních rovnic.
Diferenciální rovnice jsou ale i ideálním nástrojem i pro modelování
růstu populací v ekologii nebo odtoku srážek z regionu. Formulovat
diferenciální rovnice již umíme díky derivacím. Teď si znalosti
prohloubíme, utřídíme. Poznáme problematiku existence a jednoznačnosti
řešení. Naučíme se redukovat počet parametrů v modelu popisujícím
přírodní proces díky zavedení bezrozměrných veličin.*

      * [Přednáška 6](https://robert-marik.github.io/matematika/ode) (Diferenciální rovnice)
      * [Cvičení 7](https://robert-marik.github.io/matematika/cviceni/cviceni07.html) (Diferenciální rovnice)

### Lineární algebra

1. ![07.jpg](/images/mtk/07.jpg)  
*V materiálovém inženýrství potřebujeme často zohlednit, že v jednom
směru má materiál jiné vlastnosti než ve směru jiném. Příroda má v
materiálu jakési dálnice pro transport vody nebo tepla. Matice, které
poznáme na této přednášce, jsou skvělým prostředkem pro zachycení tohoto
jevu. Také matice poznáme jako nástroj na studium deformací materiálu.
Podíváme se i na vedení tepla, zatím bez rovnice vedení tepla.*

      * [Přednáška 7](https://robert-marik.github.io/matematika/matice) (Lineární algebra (operace s vektory a maticemi))
      * [Cvičení 8](https://robert-marik.github.io/matematika/cviceni/cviceni08.html) (Matice)

1. ![08.jpg](/images/mtk/08.jpg)
*Má-li materiál v jednom směru výrazně odlišné vlastnosti než ve směru
jiném, můžeme tuto vlastnost zohlednit v matematickém modelu a snažit se
najít směry, ve kterých je popis úlohy nejjednodušší. Týká se zejména
dřeva, které má silně odlišné vlastnosti v různých směrech. Ukážeme si,
jak najít tyto zásadní směry (využívá se řešení soustav lineárních
rovnic, které si představíme příště) a jak se pomocí nich dají
zjednodušit materiálové charakteristiky (diagonalizace matice).*

      * [Přednáška 8](https://robert-marik.github.io/matematika/inverzni_matice) (Inverzní matice, determinanty)
      * [Cvičení 9](https://robert-marik.github.io/matematika/cviceni/cviceni09.html) (Determinanty, soustavy rovnic)

1. ![09.jpg](/images/mtk/09.jpg)
*Při řešení praktických úloh sice pomocí fyziky zpravidla snadno
sestavíme diferenciální rovnici popisující daný jev, ale vyřešit rovnici
efektivně bývá i v relativně jednoduchých případech nemožné. Například
velice záleží na geometrii úlohy, tj. tvaru studovaného tělesa apod.
Zpravidla se takové úlohy převádí na řešení soustav lineárních rovnic.
Proto soustavy patří k malé násobilce inženýra a v této přednášce se je
mimo jiné naučíme řešit numericky.*

      * [Přednáška 9](https://robert-marik.github.io/matematika/soustavy) (Soustavy lineárních rovnic)
      * [Cvičení 10](https://robert-marik.github.io/matematika/cviceni/cviceni10.html) (Vlastní čísla a směry)

### Transportní děje v přírodě

1. ![10.jpg](/images/mtk/10.jpg)
*Zákony zachování jsou základními stavebními kameny mnoha technických
výpočtů zabývajících se transportem látky, energie, či jakékoliv
veličiny. Prakticky všechny mají jednotné matematické pozadí a stejnou
formu (rovnice kontinuity, resp. rovnice difuze, resp. rovnice vedeni
tepla), kterou si představíme v této přednášce. Ukážeme si jednotný
aparát pro popis sušení dřeva, vedení tepla, proudění vody v korytě a
proudění podzemní vody.*

      * [Přednáška 10](https://robert-marik.github.io/matematika/vektorove_pole) (Vektorová pole, tok, zákony zachování)
      * [Cvičení 11](https://robert-marik.github.io/matematika/cviceni/cviceni11.html) (Parciální derivace, rovnice vedení tepla)

### Ostatní

1. ![11.jpg](/images/mtk/11.jpg) *Integrály je někdy nutné uvažovat i ve více proměnných. Třeba pokud veličina, kterou studujeme, není rozložena v jedné dimenzi podél přímky, ale v rovině. Technické aplikace jsou například při studiu odolnosti nosníků vůči deformaci (kvadratický moment průřezu). Geometrické aplikace jsou například při výpočtech objemů těles nepravidelného tvaru, jako jezero se známým profilem dna.* 
      * [Přednáška 11](https://robert-marik.github.io/matematika/dvojny_integral) (Dvojný integrál)
      * [Cvičení 12](https://robert-marik.github.io/matematika/cviceni/cviceni12.html) (Dvojný integrál)

1. ![12.jpg](/images/mtk/12.jpg) *Numerické modelování je silná zbraň, ale množství parametrů, které je
nutno nastavit, by úlohu komplikovalo. Na rovnici vedení tepla si
ukážeme zavedení bezrozměrných veličin, které toto množství parametrů
sníží. Navazuje na problematiku transformace diferenciální rovnice do
bezrozměrných veličin. To jsme nakousli během semestru a teď si
dovednosti rozšíříme. Ukážeme si výstupy některých numerických metod.*

      * [Přednáška 12](https://robert-marik.github.io/matematika/numerika/) (Vybrané postupy numerické matematiky)
</div>


*Obrázky: pixabay.com, R. Mařík, R. Slávik, J. Dömény*


