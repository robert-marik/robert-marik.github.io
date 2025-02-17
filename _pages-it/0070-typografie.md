---
title: Matematika a typografie
author: Robert Mařík
date: 2021-01-01
layout: post
permalink: typografie
---



## Typografické zásady

* Matematický výraz se ve větě chová jako běžné slovo. 
* Uvnitř věty nikdy nekončí odstavec a nezačíná odstavec další.
* Důležité rovnice píšeme na samostatný řádek. Ale ani tehdy nerušíme předchozí pravidlo. Systémy mívají schopnosti vycentrovat rovnici na samostatném řádku i bez ukončení odstavce uvnitř věty. 
* Nezapomínáme tečku na konci věty. I když je posledním "slovem" rovnice.
* Matematické proměnné píšeme speciálním druhem písma, matematickou kurzívou. Značky fyzikálních veličin, jména funkcí a některé další symboly (například písmeno "d" v diferenciálech) píšeme textovým fontem.
* Mezi číslem a jednotkou a v dalších situacích vkládáme mezery dle zvyklostí a norem a dle možností systému, ve kterém text pořizujeme. 

[Video Nepište texty obsahující matematiku se školáckými typografickými chybami](https://youtu.be/yR57IHcZNyo)

## Praktické rady a ukázky

####  Věta obsahující matematický text je pořád věta

Věta začíná velkým písmenem, končí tečkou, uvnitř věty nekončí
odstavec a nezačíná nový odstavec.

> Toto je první věta odstavce. Odstavec obsahuje více vět. Asi
  nejslavnější rovnicí fyziky je Einsteinova rovnice \\[E=mc^2,
  \tag{*}\\] kde $m$ je hmotnost a $E$ je energie. Všimněte si, že jsem
  nezačínal odstavec, tj. že ve zdrojovém textu pro Markdown nebo
  LaTeX není prázdný řádek. Ani před rovnicí, ani za rovnicí, ani nikde
  jinde uvnitř odstavce.

####  Není nutné psát před každou rovnici dvojtečku

Naopak. Je velmi málo případů, kdy se hodí před rovnici dvojtečku
napsat. Pokud pro tohle nemáte cit a zkušenosti, nejjednodušším řešením
je nepsat ji nikde (a případně upravit formulaci textu). Anebo si
prostudovat pravidla pravopisu a pročíst spoustu dobře napsaných knih
v jazyce, který používáte pro psaní. (Tedy ne skripta ani webové
prezentace, ale kvalitní knihy, které prošly rukama editora a
typografa.).

Tady by to s dvojtečkou ještě šlo.

> Kořeny kvadratické rovnice vypočítáme podle následujícího vztahu: \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.\\]

Ale i tak je lepší některá z následujících variant (rovnice mimo větu
anebo vynechání slova "následujícího"). Mě se víc líbí druhá, protože
je kratší a stejně srozumitelná.

> Kořeny kvadratické rovnice vypočítáme podle následujícího vztahu. \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\\]

> Kořeny kvadratické rovnice vypočítáme ze vztahu \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.\\]


#### Čárky a tečky píšeme podle pravidel pravopisu

Například před spojkou "kde" se píše čárka. To platí i pokud předchozí
text končí rovnicí, viz příklad výše s Einsteinovou rovnicí. Podobně zacházíme s koncem věty.

> Asi nejslavnější rovnicí fyziky je Einsteinova rovnice
  \\[E=mc^2. \tag{*}\\] To je příklad věty, která končí rovnicí. Proto
  za touto rovnicí je tečka.

#### Výčet, odrážky

Výčet se píše příkazy pro výčet. Není prostor pro ruční formátování.

* Nepoužívají se tvrdé konce řádku ani odstavce.
* V Markdownu například pomocí hvězdičky.
* V LaTeXu pomocí prostředí typu enumerate, itemize, ...
* Ve Wordu pomocí odrážek.

#### Matematické výrazy píšeme jako matematické výrazy

Každý matematický objekt musí být zapsán jako matematický objekt,
tj. v dolarech u Mardown/LaTeX nebo příslušnou volbou ve Wordu. To
platí i když se jedná o jedno písmenko, jako například $m$ nebo $E$ v
 příkladě výše s Einsteinovou rovnicí.

#### Fyzikální jednotky se píšou jiným písmem než proměnné

Mezi numerickou hodnotou a jednotkou se píše zúžená mezera (pokud to
program který používáme umí). Jestli psát tečky nebo mezery pro
násobení nechejme na zvyklostech v oboru. Například tíhové zrychlení
je $g=9{,}81 \,
\mathrm{kg}\cdot\mathrm{m}\cdot\mathrm{s^{-2}}$. Všimněte se mezery
mezi číslem a jednotkou a rozdílného fontu u označení veličiny a
jednotky.

#### Text jako matematický objekt

Pokud dáváme do matematického výrazu text, je nutné jej označit jako
text. Například hustotu počítáme podle vztahu
\\[\text{hustota}=\frac{\text{objem}}{\text{hmotnost}}.\\] Někdy je indexem text, například můžeme pracovat s teplotou  venku ($T_{\text{venku}}$).

####  Vysvětlení veličin

Pokud vysvětlujeme veličiny vystupující v rovnici není vhodné používat
pomlčky anebo pomlčky následované slovesem "je". Nejjednodušší je
použít postup použitý výše, tj. pomocí slovesa je. Další
možností je přehlednější formátování, ale v tomto případě je nutné
vyřešit zarovnání. Například výčet (definition list) nebo tabulka.

####  Věta nezačíná číslem nebo rovnicí

Není pěkné začít větu rovnicí. Pár slov na úvod udělá text čtivější.

####  Označení veličin musí být konzistentní v celém textu

Není možné jednu a tu stejnou veličinu psát více způsoby. Například,
pokud používáme veličinu $\gamma_M$, není možné na jiném místě
dokumentu psát $\gamma M$. (Písmeno $M$ je jednou jako dolní index a
podruhé ne.)

####  Každá věta musí dávat smysl

Každá věta musí být správně utvořená a musí dávat smysl.  Zejména první
slovo vždy začíná velkým písmenem, na konci věty je tečka. Většina vět
obsahuje přísudek a podmět.

####  Pokud něco neumím, tak se tomu vyhnu a řeknu to jinak

Pokud jste autory nebo překladateli textu a nejste si jisti nějakou
větnou konstrukcí, nepoužívejte ji a snažte se věc říci jiným
způsobem. Jednodušší vyjádření myšlenek je často lepší.

####  Každý znak má svůj význam

Nepíšeme žádný znak v kontextu, ve kterém se nepoužívá. 

* Například tečka za koncem věty je jiná než tečka pro násobení. Tečka
pro násobení je speciální znak který je uprostřed řádku a má mezerování jako binární operátor.
* Derivace se označuje apostrofem nebo speciálním příkazem pro
derivaci. Není možné pro derivaci použít zpětný apostrof, lomítko v
horním indexu a podobně.
* Značku pro implikaci není možné seskládat z rovnítka a znaku ostře větší.
* Křížek pro násobení a písmeno x jsou jiné znaky.

| požadovaný výstup | špatný zápis |
|--------| ------- |
| $5\cdot 2=10$    | $5.2=10$|
| $5\times 2=10$   | $5 x 2=10$  nebo $5 \text{x} 2=10$ |
|$\implies$ | $=>$|
|$1+2+3+\cdots +10$  | $1+2+3+ ... +10$|

#### Matematické značky jenom do matematických výrazů

Není vhodné vkládat matematické značky do textu. Srovnejte následující věty (z Wikipedie). Rozdíl je ve formulaci "menší než sto procent".

> Při poklesu teploty pod teplotu rosného bodu obvykle dochází ke kondenzaci vodní páry obsažené ve vzduchu, vzniká například rosa nebo mlha. Při poměrné vlhkosti $<$ 100 % je teplota rosného bodu vždy nižší než teplota vzduchu. Rozdíl mezi teplotou vzduchu a teplotou rosného bodu, který se nazývá deficit teploty rosného bodu, je tím větší, čím je menší poměrná vlhkost. 

versus

> Při poklesu teploty pod teplotu rosného bodu obvykle dochází ke kondenzaci vodní páry obsažené ve vzduchu, vzniká například rosa nebo mlha. Při poměrné vlhkosti menší než 100 % je teplota rosného bodu vždy nižší než teplota vzduchu. Rozdíl mezi teplotou vzduchu a teplotou rosného bodu, který se nazývá deficit teploty rosného bodu, je tím větší, čím je menší poměrná vlhkost. 

Druhá formulace je srozumitelná, první formulace působí dojmem, že se někde ztratila polovina nerovnice.

#### Text a vzhled textu se zapisují na jiných místech

Nadpis označíme jako nadpis a neměníme velikost písma ani font nebo
řez. Vzhled nadpisu potom vyřešíme v šabloně (šablona pro Word, css
styl pro html, hlavička dokumentu pro LaTeX). Totéž v jiných podobných
případech. Výhoda je, že změna šablony se projeví v celém
dokumentu. Při ručním formátování se musí vše procházet a opravovat.

## Komentované ukázky chybných zápisů

|Číslo|Špatně|Správně|Vysvětlení|
|-|----|----|----|
|1|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336*l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je zápis násobení. Násobení zapisujeme hvězdičkou jenom ve vstupech pro počítač. Pro texty určené lidem **hvězdičku nepoužíváme**. Nepíšeme buď nic, nebo `\times` nebo `\cdot`, tj. $1.336\times l^{0.67}$ nebo $1.336\cdot l^{0.67}$.|
|2|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 \mathrm l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je font pro proměnnou označující délku kroku. Matematické proměnné zapisujeme matematickou kurzívou. To je defaultní font v matematickém prostředí, tedy v praxi to znamená, že **nic ručně nepřepínáme**, pokud si opravdu nejsme jisti, že to je potřeba (jako například u jednotek).|
|3|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je chybějící konec věty. Na konci věty píšeme **tečku**. (Pozor, toto pravidlo nemusí platit v anglickém textu, tam záleží na typografovi publikace.)|
|4|Jednotka derivace rychlosti dinosaura podle délky kroku je $s^{-1}.$|Jednotka derivace rychlosti dinosaura podle délky kroku je $\mathrm s^{-1}.$|Špatně je font pro zápis jednotky. Úmysl byl zapsat převrácenou hodnotu sekundy, ale zapsána je převrácená hodnota dráhy. Fyzikální jednotky se nepíšou matematickou kurzívou, ta je vyhrazena pro proměnné. Přepínáme do **textového fontu** příkazem `\mathrm`.| 
|5|Jednotka derivace rychlosti dinosaura podle délky kroku je \\[\mathrm s^{-1}.\\]|Jednotka derivace rychlosti dinosaura podle délky kroku je $\mathrm s^{-1}.$|Špatně je umístění vzorce s jednotkou na samostatný řádek. Velmi krátké vzorce si umístění na **samostatný řádek** zaslouží jenom výjimečně. Například pokud vzorec potřebujeme očíslovat. Krátké matematické výrazy píšeme do textu odstavce.| 
|6|Derivace rychlosti dinosaura podle délky kroku je: \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je použití dvojtečky. Snažíme se o co nejhladší začlenění matematických výrazů do textu. Kdyby místo vzorce bylo slovo, tak taky žádnou **dvojtečku nepoužíváme**. Proto není potřeba ji psát ani v situaci, kdy je místo slova vzorec. Co není potřeba psát a nepřispívá k čitelnosti, to ani nepíšeme. (Podobně jako tečka za větou, pravidlo nemusí platit v jiných jazycích a při speciálních požadavcích typografa.)|
|7|Z Buckinghamova II teorému vyplývá pro kužel s daným úhlem u vrcholu vztah mezi objemem $V$ a výškou $h$ ve tvaru \\[V = kh^3.\\]|Pro kužel s daným úhlem u vrcholu je objem $V$ úměrný třetí mocnině výšky $h$, tj. platí \\[V = kh^3\\] pro vhodnou konstantu $k$.|Špatně je název věty, v názvu není římská dvojka, ale velké řecké písmeno "pí". Obecně platí, že **ve vlastních textech používáme jenom takové informace, o kterých jsme stoprocentně přesvědčeni, že jsou správně.** Pokud si například nejsme jisti názvem věty, v naprosté většině textů je možné se mu vyhnout.|
|8|$k$ je konstanta úměrnosti.|Veličina $k$ je konstanta úměrnosti.|Není vhodné začínat větu matematickým výrazem. Vždy je možné použít formulaci, kdy **věta začíná běžným slovem**. Poté je možné toto slovo napsat s velkým písmenem na začátku a je zcela zřejmé, že zde začíná nová věta.|

