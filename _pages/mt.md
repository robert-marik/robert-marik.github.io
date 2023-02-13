---
title: Matematika
author: Robert Mařík
date: 2023-02-01
category: Jekyll
layout: predmet
---


{% include float_image.html image_path="/images/mtk_logo.jpg" description='V 21. století má každý nástroje pro simulace na dosah ruky. I pojetí matematiky je proto vhodné posunout od "jak vypočítat jednoduchý příklad" k "jak naformulovat a zadat užitečný model". Na obrázku je měření teplotního toku dřevěným panelem ve VCJR v Útěchově. Popis transportu energie a hmoty bude jeden z našich hlavních cílů.' %}


Tato stránka obsahuje materiály pro letní semestr 2022/2023, tj. jaro a léto 2023.

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

## Rozcestník elektronických informačních zdrojů

Následující nástroje jsou kriticky důležité pro studium.

* Webová stránka, kterou právě čtete. Veřejně přístupné informace
dlouhodobějšího charakteru. Je zde rozpis výuky pro jednotlivé týdny, odkazy na učební materiály, informace 
k ukončení předmětu. 
* WeBWorK je primární nástroj pro kontrolu a evidenci odevzdávání domácích
úloh. Ty nejsou povinné, ale značně usnadní situaci u závěrečné zkoušky. <https://um.mendelu.cz/webwork2/MTK_2022/>
* Univerzitní informační systém použijeme pro hromadné maily (zkontrolujte si, že čtete mailovou adresu, na kterou případně maily z UISu přeposíláte) přihlašování na zkoušky a pro distribuci hesel pro WeBWorK. <https://is.mendelu.cz>


* Přednášky. Materiály, které se budou používat na přednášce, ale
jsou vhodné v případě nemoci i pro samostudium a jako referenční
příručka ke zkoušce. 

\<col xs="6" md="4"\> \<panel type="warning" title="Cvičení"\> Materiály
pro cvičení. V podobném formátu jako přednášky.

[Otevřít](this>../mtk/mat-slidy/cviceni/cviceni00.md.html) \</panel\>
\</col\>

\<col xs="6" md="4"\> \<panel type="warning" title="Cheatsheet"\>

Cheatsheet pro Matematiku. Vzorce, důležitá fakta.

[Otevřít](https://raw.githubusercontent.com/robert-marik/mat-slidy/master/cheatsheet/cheatsheet-MT.pdf)

\</panel\> \</col\>

\<!-- \<col xs="6" md="3"\> \<panel type="warning" title="IT
cheatsheet"\>

Cheatsheet pro věci související s IT: WeBWorK a LaTeX. Základní příkazy.

[Otevřít](https://raw.githubusercontent.com/robert-marik/hw-webwork/master/cheatsheet/cheatsheet.pdf)
\</panel\> \</col\> --\>

\</grid\>

\<markdown\>

Kombinovaná forma

------------------------------------------------------------------------

Vše je stejné jako pro presenční formu

\</markdown\>
\<markdown\>

Presenční forma

------------------------------------------------------------------------

\</markdown\>

\<panel type="danger" title="Aktuality"\>

-   Koncem týdne odejte informační mail. Budou se pravidelně otevírat po
    týdnech domácí úkoly. Pravidla stejná jako během normální výuky (ne
    konzultační)

\</panel\>

<div class="new">
<div class="f">

</div>

\<markdown\>

Legenda k semaforu a rozpisu přednášek:

\* \<span style="color:green"\>**zelená ikonka**\</span\> = proběhlo, \*
\<span style="color:red"\>**červená ikonka**\</span\> = probíhá tento
týden (přednáška a všechna cvičení), \* **šedá ikonka** = bude náplní v
dalších týdnech, na tuto látku se teprve těšíme, ale kdo jede svým
tempem se tomu už může věnovat.

Semafor se přepíná někdy během víkendu a až vše zezelená, budeme mít
látku probránu. Rozpis je orientační, může být upravován během semestru
podle aktuální situace. Některá cvičení mohou zůstat pozadu vlivem
státních svátků a dalších vlivů, vždy se proto řídíte pokyny cvičícího.

\</markdown\>

\<!-- \<panel type="warning" title="Časové rozvržení výuky"\>

-   Cvičení bývají z organizačních důvodů zpravidla tematicky k
    přednášce z předešlého týdne.
-   Domácí úloha se zpravidla otevírá v den, kdy se látka z této úlohy
    probírá na přednášce a uzavírá týden poté, co se látka probere ve
    cvičení.
-   Na oborech, kde je hlavní cvičení v době přednášky (krajinářství
    17.10.) je v tomto týdnu přednáška buď jako samostudium, nebo se
    studenti mohou zúčastnit dobrovolně (přednáška je večer, až po
    návratu z hlavního cvičení).
-   Na oborech, kde cvičení koliduje se státním svátkem nebo hlavním
    cvičením se řídíte pokyny cvičícího. Termíny odevzdání domácích úloh
    budou společné pro všechny obory a nastaveny tak, aby i ta skupina,
    která je nejvíce pozadu, měla alespoň týden na vypracování.

\</panel\> --\>

\<panel type="primary" title="Výuka konzultační formou, LS 2022/2023"\>
Materiály jsou ze zimního semestru. Proto jsou organizovány stejně, jako
byly nachystány na výuku - tj. cvičení zaostává týden za přednáškou. K
úlohám za cvičení jsou přidány úlohy z přednášky tak, aby to k sobě
tematicky pasovalo. Proto se domácí úloha zpravidla vztahuje k přednášce
z minulého týdne a cvičení z aktuálního týdne. Ale není to pravidlem, je
to prostě uděláno stejně, jako to probíhalo minulý semestr. \</panel\>

\<markdown\>

0\. \![0.jpg\](../mtk/mat-slidy/pics/0.jpg) \*Start semestru. \[Úvodní
informace\](doku.php?id=matematika-uvod).\<BR\>\<BR\>\<span
style='color:red'\>Login pro domácí úkoly je stejný jako login do
UIS.\</span\>\<BR\>\<span style='color:red'\>Heslo najdete v UIS podle
\[tohoto návodu\](<https://user.mendelu.cz/marik/login_webwork.png>),
tj. přes "List záznamníku učitele" a v něm "Průběžné
hodnocení".\</span\> (Návod vznikl před dvěma roky, pokud je aktuální
design UIS jiný, prosím o případnou aktualizaci a velmi za ni děkuji.)\*

     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/00_Uvod/)

1\. 20.2.2023
\[\![01.jpg\](../mtk/mat-slidy/pics/01.jpg)\](../mtk/mat-slidy/derivace_I)
\*Přednáška o derivacích, základním stavebním kamenu pro studium funkcí.
Naučíme se matematicky popsat rychlost. Ve cvičení se naučíme derivovat
a tuto znalost využijeme v týdnech bezprostředně následujících. Naučíme
se například pro veličiny spojené fyzikálním vzorcem najít souvislost
mezi rychlostmi změn těchto veličin. Jedna z aplikací je měření odporu
dřeva pro stanovení vlhkosti.\*

     * [Přednáška](../mtk/mat-slidy/derivace_I)
     * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni01.md.html)
     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/01_Vypocet_derivace/)

1\. 27.2.2023
\[\![02.jpg\](../mtk/mat-slidy/pics/02.jpg)\](../mtk/mat-slidy/derivace_II)
\*Naučíme se využít derivace k rozumné aproximaci funkcí a fyzikálních
zákonů. Tím se mnoho vztahů stane významně jednoduššími a matematické
modely se stanou spočitatelnými i bez superpočítačů. Ukážeme si dále
polynomiální aproximaci, která umožní zachytit jevy z podstaty
nelineární, jako je například laser. Ale rozebereme si i řešitelnost
rovnic a možnosti jejich numerického řešení.\*

     * [Přednáška](../mtk/mat-slidy/derivace_II)
     * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni02.md.html)
     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/02_Aplikace_derivace/)

1\. 6.3.2023
\[\![03.jpg\](../mtk/mat-slidy/pics/03.jpg)\](../mtk/mat-slidy/derivace_III)
\*Další využití derivací, tentokrát zaměřeno na extrémy. Naučíme se
hledat optimální stavy systému. Ukážeme si příklady v souladu s intuicí
(pokud chci vyřezat co nejtužší nosník z kulatiny, musím řezat
obdélníkový profil) i jdoucí proti intuici (tlustší izolace okolo horké
trubky nemusí znamenat menší tepelné ztráty, existuje takzvaný kritický
poloměr izolace). Seznámíme se s pojmem gradient, který dokáže
identifikovat směr podnětů dávajících do pohybu vedení tepla nebo
transport látek. A poprvé se seznámíme s bezrozměrnými veličinami, které
přijdou ke slovu i později.\*

     * [Přednáška](../mtk/mat-slidy/derivace_III)
     * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni03.md.html)
     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/03_Dalsi_aplikace_derivace/)

1\. 13.3.2023
\[\![04.jpg\](../mtk/mat-slidy/pics/04.jpg)\](../mtk/mat-slidy/integraly)
\*Derivaci jsme poznali jako míru měřící rychlost změn a nyní si uvedeme
opačnou úlohu. Znalost rychlosti s jakou se mění nějaká veličina nám
umožní najít tuto veličinu. Naučíme se například najít změnu teploty u
procesu, u kterého intenzita tepelné výměny klesá s časem.\*

     * [Přednáška](../mtk/mat-slidy/integraly)
     * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni04.md.html)
     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/04_Integraly_1/)

1\. 20.3.2023
\[\![05.jpg\](../mtk/mat-slidy/pics/05.jpg)\](../mtk/mat-slidy/integraly2)
\*Integrály pro pokročilé. Naučíme se numericky aproximovat určitý
integrál a dokonce otevřeme vrátka mimo svět elementárních funkcí.\*

     * [Přednáška](../mtk/mat-slidy/integraly2)
     * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni05.md.html)
     * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/05_Integraly_2/)

1\. 27.3.2023
\[\![06.jpg\](../mtk/mat-slidy/pics/06.jpg)\](../mtk/mat-slidy/ode)
\*Fyzikální zákony formulujeme pomocí rychlostí změn (derivací) a
důsledky hledáme řešením vzniklých rovnic, zpravidla vhodným
integrováním. Problematika spadá do oblasti diferenciálních rovnic.
Diferenciální rovnice jsou ale i ideálním nástrojem i pro modelování
růstu populací v ekologii nebo odtoku srážek z regionu. Formulovat
diferenciální rovnice již umíme díky derivacím. Teď si znalosti
prohloubíme, utřídíme. Poznáme problematiku existence a jednoznačnosti
řešení. Naučíme se redukovat počet parametrů v modelu popisujícím
přírodní proces díky zavedení bezrozměrných veličin.\*

      * [Přednáška](../mtk/mat-slidy/ode)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni06.md.html)
      * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/06_Diferencialni_rovnice/)

1\. 3.4.2023
\[\![07.jpg\](../mtk/mat-slidy/pics/07.jpg)\](../mtk/mat-slidy/matice)
\*V materiálovém inženýrství potřebujeme často zohlednit, že v jednom
směru má materiál jiné vlastnosti než ve směru jiném. Příroda má v
materiálu jakési dálnice pro transport vody nebo tepla. Matice, které
poznáme na této přednášce, jsou skvělým prostředkem pro zachycení tohoto
jevu. Také matice poznáme jako nástroj na studium deformací materiálu.
Podíváme se i na vedení tepla, zatím bez rovnice vedení tepla.\*

      * [Přednáška](../mtk/mat-slidy/matice)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni07.md.html)
      * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/07_Matice/)

1\. 10.4.2023
\[\![08.jpg\](../mtk/mat-slidy/pics/08.jpg)\](../mtk/mat-slidy/inverzni_matice)
\*Má-li materiál v jednom směru výrazně odlišné vlastnosti než ve směru
jiném, můžeme tuto vlastnost zohlednit v matematickém modelu a snažit se
najít směry, ve kterých je popis úlohy nejjednodušší. Týká se zejména
dřeva, které má silně odlišné vlastnosti v různých směrech. Ukážeme si,
jak najít tyto zásadní směry (využívá se řešení soustav lineárních
rovnic, které si představíme příště) a jak se pomocí nich dají
zjednodušit materiálové charakteristiky (diagonalizace matice). \<span
style="color:red"\>Domácí úkol se vztahuje i k látce z následujícího
týdne.\</span\>\*

      * [Přednáška](/marik/mtk/mat-slidy/inverzni_matice)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni08.md.html)
      * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/08_Matice_a_vlastni_vektory/)

1\. 17.4.2023
\[\![09.jpg\](../mtk/mat-slidy/pics/09.jpg)\](../mtk/mat-slidy/soustavy)
\*Při řešení praktických úloh sice pomocí fyziky zpravidla snadno
sestavíme diferenciální rovnici popisující daný jev, ale vyřešit rovnici
efektivně bývá i v relativně jednoduchých případech nemožné. Například
velice záleží na geometrii úlohy, tj. tvaru studovaného tělesa apod.
Zpravidla se takové úlohy převádí na řešení soustav lineárních rovnic.
Proto soustavy patří k malé násobilce inženýra a v této přednášce se je
mimo jiné naučíme řešit numericky.\*

      * [Přednáška](/marik/mtk/mat-slidy/soustavy)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni09.md.html)

1\. 24.4.2023
\[\![10.jpg\](../mtk/mat-slidy/pics/10.jpg)\](../mtk/mat-slidy/vektorove_pole)
\*Zákony zachování jsou základními stavebními kameny mnoha technických
výpočtů zabývajících se transportem látky, energie, či jakékoliv
veličiny. Prakticky všechny mají jednotné matematické pozadí a stejnou
formu (rovnice kontinuity, resp. rovnice difuze, resp. rovnice vedeni
tepla), kterou si představíme v této přednášce. Ukážeme si jednotný
aparát pro popis sušení dřeva, vedení tepla, proudění vody v korytě a
proudění podzemní vody.\*

      * [Přednáška](/marik/mtk/mat-slidy/vektorove_pole)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni11.md.html)
      * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/09_Difuzni_rovnice/)

1\. 1.5.2023
\[\![11.jpg\](../mtk/mat-slidy/pics/11.jpg)\](../mtk/mat-slidy/dvojny_integral)

      *Integrály je někdy nutné uvažovat i ve více proměnných. Třeba pokud veličina, kterou studujeme, není rozložena v jedné dimenzi podél přímky, ale v rovině. Technické aplikace jsou například při studiu odolnosti nosníků vůči deformaci (kvadratický moment průřezu). Geometrické aplikace jsou například při výpočtech objemů těles nepravidelného tvaru, jako jezero se známým profilem dna. <span style="color:red">Domácí úloha je už jenom opakování.</span>* 
      * [Přednáška](/marik/mtk/mat-slidy/dvojny_integral)
      * [Cvičení](/marik/mtk/mat-slidy/cviceni/cviceni12.md.html)
      * [Domácí úkol](http://um.mendelu.cz/webwork2/MTK_2022/10_Shrnuti/)

1\. 8.5.2023
\[\![12.jpg\](../mtk/mat-slidy/pics/12.jpg)\](../mtk/mat-slidy/numerika)
\*Numerické modelování je silná zbraň, ale množství parametrů, které je
nutno nastavit, by úlohu komplikovalo. Na rovnici vedení tepla si
ukážeme zavedení bezrozměrných veličin, které toto množství parametrů
sníží. Navazuje na problematiku transformace diferenciální rovnice do
bezrozměrných veličin. To jsme nakousli během semestru a teď si
dovednosti rozšíříme. Ukážeme si výstupy některých numerických metod.\*

      * [Přednáška](/marik/mtk/mat-slidy/numerika/)

\<!--

\[\![14.jpg\](../mtk/mat-slidy/pics/14.jpg)\](../mtk/mat-slidy/shrnuti)
\*Poslední týden výuky. Na přednášce i ve cvičení se budeme věnovat
závěrečnému shrnutí a utřídění poznatků. U oborů kde cvičení odpadlo
vinou státního svátku nebo hlavního cvičení se dokončí látka ze cvičení.
U oborů, kde cvičení neodpadlo, bude opakování a shrnutí.\*

      * [Přednáška](/marik/mtk/mat-slidy/shrnuti/)

1\. Závěrečné opakování \*procvičujte, zkoušejte si již proběhnuté
písemky, dělejte si výpisky podstatných informací, abyste se v nich
uměli orientovat a vštípili si je do hlavy a měli tak dobrý základ k
tomu, abyste z těchto znalostí mohli těžit celý život.\* --\>

\</markdown\>
<!--
1. [![13.jpg](../mtk/mat-slidy/pics/13.jpg)](../mtk/mat-slidy/) *Jdeme do finiše. K některým pojmům má smysl se vrátit. Nyní s kvalitnějšími nástroji než jsme měli v době, kdy jsme se s nimi seznámili poprvé.*
   * Přednáška: Nevešlo se (koronavir)
   * Cvičení: Nevešlo se (koronavir)
1. [![14.jpg](../mtk/mat-slidy/pics/14.jpg)](../mtk/mat-slidy/) **Rezerva pro případ hlavního cvičení nebo vstup do reálného světa představením vybrané aplikace matematiky.**
   * Přednáška: Nevešlo se (koronavir)
   * Cvičení: Nevešlo se (koronavir)
-->
</div>

\<markdown\>

Doplňková literatura

------------------------------------------------------------------------

(základní literaturou jsou přednášky a cvičení výše)

\*
\[Playlist\](<https://www.youtube.com/playlist?list=PLTcG-zIT2ivUGVSgc25TjSg4ENZi3Bwij>)
s videi ze zimního semestru 2020. Dobré pro začátek a vhodné pro
studenty se slabšími matematickými dovednostmi, ale postupně (každý dle
svých schopností a preferencí) věnujte méně času videím a více času
tištěnému textu. \* Učebnice \[Došlá, Z., Liška, P., Matematika pro
nematematické obory s aplikacemi v přírodních a technických
vědách.\](<http://www.modreknihkupectvi.cz/product.php?id_product=2349>) 1.
vyd. Praha: Grada Publishing, a.s., 2014. 304 s. ISBN 978-80-247-5322-5.
\* Skripta Rádl, P., Černá, B., Stará, L, Základy vyšší matematiky, 3.
vyd. Brno: Mendelova univerzita v Brně, 2014. 176 s. ISBN
978-80-7509-110-9. \* \[Vzorce a triky pro derivace a
integrály\](/marik/mt/vzorce.pdf) \* \[Playlist s domácími úkoly z roku
2020\](<https://www.youtube.com/playlist?list=PLTcG-zIT2ivXZpHu2yL2oqsdKRCF87QjL>),
kdy byly úlohy ve WeBWorKu velice podobné tomu, co je zadáváno letos. \*
\[Odznáčky ve WeBWorKu\](<https://um.mendelu.cz/achievementsMTK.html>) -
porovnejte se se spolužáky, jak jste aktivní a kolik máte odměn nebo
jaký máte level za splněné domácí úkoly. Čím víc, tím lepší šance projít
zkouškou v pohodě a bez dalšího učení.

\<!-- \### Materiály z předchozích let

\* \[Moje materiály\](?id=matematika_old) z let 2018-2019 \*
\[Přednášky\](/marik/mt/prednasky/) z letního semestru 2019 \*
\[Cvičení\](/marik/mt/cviceni/) z letního semestru 2019 \* \[Moje
materiály\](?id=matematika_old2) z let 2009 až 2011 \*
\[Materiály\](<http://user.mendelu.cz/smykalov/>) dr. Smýkalové, do roku
2018 --\>

\</markdown\>

## Ukončení

\<panel type="warning" title="Požadavky na ukončení"\>

-   Během semestru budou zadávány domácí úlohy v systému
    [WeBWorK](http://um.mendelu.cz/webwork2/MTK_2022). Nejsou povinné,
    ale mohou značně pomoci u zkoušky.
-   Zápočty se neudělují, vše se rozhoduje u zkoušky. Přihlašování na
    zkoušky přes univerzitní informační systém. Počet pokusů dle
    [studijního a zkušebního
    řádu](https://is.mendelu.cz/dok_server/slozka.pl?download=265502)
    (jeden řádný a dva opravné pokusy). Termíny budou oznámeny podle
    studijního a zkušebního řádu nejpozději dva týdny před začátkem
    zkouškového.
-   **Závěrečná písemná zkouška na 50 bodů.** Je možné používat
    literaturu, není možné používat přístup na Internet ani elektronické
    nosiče informací. Musí být splněny současně dvě následující
    podmínky.

<!-- -->

          * Písemku je nutno napsat alespoň na 15 bodů.
          * Součet bodů za písemku a bonusových bodů za domácí úkoly musí být alespoň 25  bodů.
    * **Bonus za domácí úkoly je nevýše 20 bodů.** Součet za všechny úlohy je 160 bodů, body vidíte ve [[https://um.mendelu.cz/webwork2/MTK_2022/grades/|WeBWorKu v levém panelu pod položkou Hodnocení]] ve sloupci "Celkem". (Sloupce s procenty a celkovým maximem budou sedět až budou otevřeny všechny úlohy.) Bonusy jsou přidělovány následovně:
         * 20 bonusových bodů za hodnocení alespoň 90% bodů z domácích úloh, tj. alespoň 144 bodů,
         * 15 bonusových bodů za alespoň 70% bodů z domácích úloh, tj. alespoň 112 bodů,
         * 10 bonusových bodů za alespoň 60% bodů z domácích úloh, tj. alespoň 96 bodů, 
         * 6 bonusových bodů za alespoň 50% bodů z domácích úloh, tj. alespoň 80 bodů.
         * 4 bonusové body za alespoň 33% bodů z domácích úloh, tj. alespoň 53 bodů.
    * Antiplagiátorská a antighostwritingová ochrana: podle možností, epidemiologické situace a dalších okolností bude vybrané části zkoušky v některých případech nutno obhájit krátkým rozhovorem (ústní zkoušení). Teprve tímto bude potvrzena známka podle následujícího klíče.
         * **Hodnocení A (56-70 bodů),**
         * **Hodnocení B (48-55 bodů),**
         * **Hodnocení C (41-47 bodů),**
         * **Hodnocení D (33-40 bodů),**
         * **Hodnocení E (25-32 bodů),**
         * **Hodnocení F - nevyhověl/a.**
    * Příklady a ukázky hodnocení	   
         * Pokud student neplnil domácí úlohy, počítají se jenom body z písemky. Například zisk 40 bodů na písemku znamená hodnocení D.
         * Pokud student má za domácí úlohy 10 bonusových bodů a za písemku 15 bodů, je celkové hodnocení E (25 bodů celkem).
         * Pokud student má za domácí úlohy 20 bonusových bodů a za písemku 10 bodů, je celkové hodnocení F (není dosažena minimální hranice písemky)
         * Pokud má student za domácí úlohy 20 bonusových bodů, stačí mu písemku napsat na minimum 15 bodů. Známka bude přinejhorším D. Méně než 15 bodů znamená F.
    * Materiály ke zkoušce
         * Zde na webu, doporučená literatura zde na webu a v sylabu
         * Přímý odkaz na přednášky v [[http://user.mendelu.cz/marik/mtk/mat-slidy/mat_slidy_all.pdf|PDF]]
         * Přímý odkaz na cvičení v [[https://user.mendelu.cz/marik/mtk/mat-slidy/cviceni/cviceni.pdf|PDF]]

\</panel\>

\<panel type="warning" title="Obsah zkoušky"\>

-   **Závěrečná písemná zkouška:**

<!-- -->

       * Ukázkou zadání jsou [[this>../mtk/pisemky/2021_ZS/|písemky ze zimního semestru 2021/2022]]. 
       * Vzhledem k možnosti používat literaturu bude důsledný požadavek na odpovídání k věci. **Neopisujte chaoticky sáhodlouhé texty. Neplýtvejte časem na třeba správná tvrzení, která nejsou odpovědí a bude na ně tedy brán spíše negativní zřetel.**
       * Odpověď musí dávat smysl. Každý rok narážíme na to, že si studenti neuvědomí, že pokud se z kvalitního správného textu vytrhne **bez kontextu a bez myšlenky náhodný kus** a použije jako odpověď na nějakou otázku, zpravidla taková odpověď nebývá správná a ani smysluplná. 
       * Jsou preferovány **stručné** formulace, klidně heslovité, avšak **úplné** a **k věci**. 
    * **Staré písemky**
        * Staré offline písemky jsou [[this>../mtk/pisemky/2019_ZS/|zde]] a [[this>../mt/pisemka|zde]] (ještě starší [[this>../mt/pisemka_2019/|zde]]), ale jedná se o písemky, které byly psány bez možnosti používat vlastní poznámky. Proto bude formulace teoretických otázek taková, aby bylo zohledněno to, že je možné používat literaturu. Také písemky obsahují některou látku, která již není aktuální, například průběh funkce.
        * Online písemky ze zimního COVIDového semestru 2020 jsou [[this>../mtk/pisemky/2020_ZS/|zde]]. Videokomentáře a řešení některých online písemek jsou v [[https://www.youtube.com/playlist?list=PLTcG-zIT2ivXZpHu2yL2oqsdKRCF87QjL|playlistu s prací v systému WeBWorK]]. Můžete si projít, ale s online formou se nepočítá, pokud nás k tomu nedonutí epidemiologická situace.

\</panel\>

\<panel type="warning" title="Co v případě neúspěchu"\>

-   V případě neúspěchu v předmětu je možnost zapsat si jej opětovně.
    Postupuje se podle Studijního a zkušebního řádu.
-   Předmět se učí jenom v zimním semestru. Nejbližší plnohodnotná výuka
    předmětu bude v zimním semestru 2023/2024 tj. na podzim 2023.
-   Pro studenty, kteří chtějí složit zkoušku v letním semestru bude
    vypsána konzultační forma předmětu (viz studijní a zkušební řád,
    jedná se jenom o složení zkoušky, nebudou probíhat ani přednášky ani
    cvičení). Protože zápis do konzultační formy je podmíněn malým
    zápočtem, ale zápočty v předmětu nemáme, bude postup následující.
    -   Na konci semestru těm co nemají zkoušku, ale prokázali jisté
        znalosti, udělím formálně zápočet, aby mohli zvážit případné
        absolvování předmětu v letním semestru konzultační formou.
    -   Prokázat jisté znalosti znamená splnit jednu z následujících
        podmínek.
        -   Přijít alespoň jednou na zkouškovou písemku a získat alespoň
            8 bodů z 50.
        -   Pracovat na domácích úkolech a mít alespoň polovinu bodů za
            domácí úkoly, tj. alespoň 80 bodů.

\</panel\>

\<markdown\> \*Obrázky: pixabay.com, R. Mařík, R. Slávik, J. Dömény\*
\</markdown\>

