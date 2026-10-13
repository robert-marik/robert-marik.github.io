---
title: Matematika a typografie
author: Robert Mařík
date: 2021-01-01
layout: post
permalink: typografie
---

<style>
  .markdown-section ul li ul li {background-color: #eeeeee; padding: 15px; margin:5px; }
  .red, .bad {color:red;}
</style>

Stránka shrnuje nejčastější typografické chyby v textech obsahujících
matematiku, například v protokolech, seminárních a závěrečných pracích.
U ukázek je značkou ✔ označen správný zápis a značkou ✘ chybný zápis.
Za ukázkou je často i zdrojový kód pro LaTeX nebo Markdown. Jak takové
texty psát technicky, je popsáno na stránce [LaTeX](latex).

[Video Nepište texty obsahující matematiku se školáckými typografickými chybami](https://youtu.be/yR57IHcZNyo)

## Rychlý přehled

| Pravidlo | ✔ Správně | ✘ Špatně | Zápis v LaTeXu |
|----|----|----|----|
| Proměnné matematickou kurzívou | $m$ | m | `$m$` |
| Jednotky textovým fontem | $\mathrm{m}\cdot\mathrm{s}^{-2}$ | $m\cdot s^{-2}$ | `\mathrm{m}\cdot\mathrm{s}^{-2}` |
| Funkce textovým fontem | $\sin x$ | $sin x$ | `\sin x` |
| Diferenciál, $\mathrm e$, $\mathrm i$ textovým fontem | $\mathrm dx$, $\mathrm e^x$ | $dx$, $e^x$ | `\mathrm dx`, `\mathrm e^x` |
| Text v rovnici jako text | $T_{\text{venku}}$ | $T_{venku}$ | `T_{\text{venku}}` |
| Násobení | $ab$, $a\cdot b$, $a\times b$ | $a*b$, $a.b$, $a\mathrm{x}b$ | `a\cdot b`, `a\times b` |
| Tři tečky | $1+2+\cdots+10$ | $1+2+...+10$ | `\cdots` |
| Implikace | $\implies$ | $=>$ | `\implies` |
| Minus | $-5$ | -5 (spojovník v textu) | `$-5$` |
| Rovnice je součástí věty | čárka, tečka za rovnicí | chybí interpunkce | `\[ E=mc^2. \]` |
| Uvnitř věty není konec odstavce | bez prázdného řádku | prázdný řádek kolem rovnice | |
| Věta nezačíná vzorcem | Veličina $k$ je … | $k$ je … | |

## Písmo (fonty)

* Proměnné se zapisují speciálním fontem vyhrazeným pro matematiku, tzv. matematickou kurzívou. Tento font je nutné použít pro odlišení matematických, fyzikálních nebo statistických veličin. To platí i v případě, že se jedná o jedno písmenko v textu. V Markdownu a LaTeXu proto i jednotlivé písmeno píšeme mezi dolary, ve Wordu jako rovnici.
  * **✔ Správně (proměnné matematickým fontem):** Tíhovou sílu $F_G$ určíme z hmotnosti tělesa $m$ vztahem \\[F_G=mg,\\]
    kde $g$ je tíhové zrychlení.<br>
    `Tíhovou sílu $F_G$ určíme z hmotnosti tělesa $m$ vztahem \[F_G=mg,\] kde $g$ je tíhové zrychlení.`
  * <span class="bad">**✘ Špatně (ve dvou případech není matematický font):** Tíhovou sílu $F_G$ určíme z hmotnosti tělesa m vztahem \\[F_G=mg,\\]
    kde g je tíhové zrychlení. </span>
* Značky jednotek fyzikálních veličin, jména funkcí a některé další symboly píšeme textovým fontem. Mezi tyto symboly patří písmeno $\mathrm d$ v diferenciálech a derivacích, Eulerovo číslo $\mathrm e$ a imaginární jednotka $\mathrm i$. Textový font zapneme v LaTeXu příkazem `\mathrm`, pro běžné funkce existují připravené příkazy (`\sin`, `\cos`, `\ln`, `\exp`, `\log`, ...).
  * **✔ Správně (jednotky textovým fontem):** Hodnota tíhového zrychlení závisí na zeměpisné šířce, v Česku bereme přibližně $g=9.81\,\mathrm{m}\cdot\mathrm{s}^{-2}$.<br>
    `$g=9.81\,\mathrm{m}\cdot\mathrm{s}^{-2}$`
  * <span class="bad">**✘ Špatně (font u fyzikální veličiny):** Hodnota tíhového zrychlení závisí na zeměpisné šířce, v Česku bereme přibližně g=9.81 ms${}^{-2}$.</span>
  * <span class="bad">**✘ Špatně (font u fyzikální jednotky):** Hodnota tíhového zrychlení závisí na zeměpisné šířce, v Česku bereme přibližně $g=9.81\,m\,s^{-2}$.</span>
  * **✔ Správně (funkce textovým fontem):** Důsledkem Pythagorovy věty na jednotkové kružnici je identita\\[\sin^2 x+\cos^2 x = 1.\\]
    `\[\sin^2 x+\cos^2 x = 1.\]`
  * <span class="bad">**✘ Špatně (funkce jsou špatným fontem):** Důsledkem Pythagorovy věty na jednotkové kružnici je identita\\[sin^2 x+cos^2 x = 1.\\]</span>
  * **✔ Správně (diferenciál a Eulerovo číslo textovým fontem):** Platí \\[\int_0^1 \mathrm e^{x}\,\mathrm dx = \mathrm e-1.\\]
    `\[\int_0^1 \mathrm e^{x}\,\mathrm dx = \mathrm e-1.\]`
  * <span class="bad">**✘ Špatně (diferenciál a Eulerovo číslo matematickou kurzívou):** Platí \\[\int_0^1 e^{x} dx = e-1.\\]</span>
* Pokud dáváme do matematického výrazu text, je nutné jej označit jako text příkazem `\text`. Někdy je textem i index.
  * **✔ Správně (text v rovnici):** Hustotu počítáme podle vztahu \\[\text{hustota}=\frac{\text{hmotnost}}{\text{objem}}.\\] Teplotu venku označíme $T_{\text{venku}}$.<br>
    `\[\text{hustota}=\frac{\text{hmotnost}}{\text{objem}}.\]`, `$T_{\text{venku}}$`
  * <span class="bad">**✘ Špatně (text v rovnici matematickou kurzívou):** Hustotu počítáme podle vztahu \\[hustota=\frac{hmotnost}{objem}.\\] Teplotu venku označíme $T_{venku}$.</span>
* Tímto způsobem se zapisují i veličiny, které mají označení složené z více než jednoho písmene. Elegantnější však je dodržovat to, že pro každou veličinu je zkratka tvořena jedním písmenem. Například místo veličiny $\text{MOE}$ (modulus of elasticity) je lepší psát $E$, případně $E_{\text{MOE}}$, nebo $E_{\text{MOE},3}$ a podobně.
* Vektory a matice se někdy zapisují tučným písmem (například $\mathbf u$, $\mathbf A$), vektory také se šipkou (například $\vec u$). Zvolíme jeden způsob a ten dodržujeme v celém textu.

## Matematika ve větě

* Věta obsahující matematický text je pořád věta. Začíná velkým písmenem a končí tečkou. Matematický výraz se ve větě chová jako běžné slovo. Pokud za ním má podle pravidel pravopisu následovat čárka nebo tečka, následuje za ním čárka nebo tečka. To platí i pro rovnici na samostatném řádku.
  * **✔ Správně (čárka před "který", "kde" apod.):** Použijeme Pythagorovu větu pro přeponu $c$, která je nejdelší stranou pravoúhlého trojúhelníka.
  * **✔ Správně (čárka za rovnicí):** Použijeme identitu \\[a^2+b^2=c^2, \\] která je známa jako Pythagorova věta.<br>
    `Použijeme identitu \[a^2+b^2=c^2, \] která je známa jako Pythagorova věta.`
  * <span class="bad">**✘ Špatně (chybí čárka):** Použijeme identitu \\[a^2+b^2=c^2 \\] která je známa jako Pythagorova věta.</span>
  * **✔ Správně (tečka na konci věty):** Objem koule o poloměru $r$ je dán vztahem \\[V=\frac 43 \pi r^3. \\]
  * <span class="bad">**✘ Špatně (chybí tečka na konci věty):** Objem koule o poloměru $r$ je dán vztahem \\[V=\frac 43 \pi r^3 \\]</span>
* Uvnitř věty nikdy nekončí odstavec a nezačíná odstavec další. Důležité rovnice píšeme na samostatný řádek, ale ani tehdy nerušíme toto pravidlo. Systémy umí vycentrovat rovnici na samostatném řádku i bez ukončení odstavce. Ve zdrojovém textu pro Markdown nebo LaTeX proto není prázdný řádek ani před rovnicí, ani za rovnicí, ani nikde jinde uvnitř odstavce. Ve Wordu rovnici necentrujeme jako samostatný odstavec, ale použijeme u rovnice volbu "Změnit na samostatný".
  * **✔ Správně (rovnice uvnitř odstavce):** Toto je první věta odstavce. Odstavec obsahuje více vět. Asi nejslavnější rovnicí fyziky je Einsteinova rovnice \\[E=mc^2,\\] kde $m$ je hmotnost a $E$ je energie. Odstavec pokračuje další větou.
  * Zdrojový text předchozí ukázky (bez prázdných řádků):
    ```
    Toto je první věta odstavce. Odstavec obsahuje více vět. Asi
    nejslavnější rovnicí fyziky je Einsteinova rovnice
    \[E=mc^2,\]
    kde $m$ je hmotnost a $E$ je energie. Odstavec pokračuje další větou.
    ```
* Krátké výrazy píšeme do textu odstavce. Na samostatný řádek dáváme jenom důležité nebo rozměrné rovnice.
* Rovnici můžeme očíslovat, pokud se na ni budeme odkazovat v dalším textu. Číslo se zpravidla zarovnává na pravý okraj. Číslujeme jenom rovnice, na které se odkazujeme. V LaTeXu rovnici označíme příkazem `\label` a odkaz vytvoříme příkazem `\eqref`, číslo se tedy nepíše ručně.
  * **✔ Správně (rovnice s číslem):** Pythagorova věta \\[a^2+b^2=c^2\tag{1}\\] je jednou z nejužitečnějších geometrických identit. Z rovnice (1) vyplývá, že přepona je nejdelší stranou.<br>
    `\begin{equation}a^2+b^2=c^2\label{eq:pythagoras}\end{equation}` a dále `Z rovnice \eqref{eq:pythagoras} vyplývá ...`
* Není nutné psát před každou rovnici dvojtečku. Naopak, je velmi málo případů, kdy se hodí před rovnici dvojtečku napsat. Kdyby místo vzorce bylo slovo, také bychom dvojtečku nepoužili. Pokud pro tohle nemáte cit a zkušenosti, nejjednodušším řešením je nepsat ji nikde (a případně upravit formulaci textu). Anebo si prostudovat pravidla pravopisu a pročíst spoustu dobře napsaných knih v jazyce, který používáte pro psaní. (Tedy ne skripta ani webové prezentace, ale kvalitní knihy, které prošly rukama editora a typografa.)
  * **✔ Správně (bez dvojtečky, nejlepší varianta):** Kořeny kvadratické rovnice vypočítáme ze vztahu \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.\\]
  * **✔ Přípustné (rovnice mimo větu):** Kořeny kvadratické rovnice vypočítáme podle následujícího vztahu. \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\\]
  * **Ještě přípustné (s dvojtečkou):** Kořeny kvadratické rovnice vypočítáme podle následujícího vztahu: \\[x_{1,2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.\\]
* Věta nezačíná číslem ani matematickým výrazem. Pár slov na úvod udělá text čtivější a je zřejmé, kde začíná nová věta.
  * **✔ Správně:** Veličina $k$ je konstanta úměrnosti.
  * <span class="bad">**✘ Špatně:** $k$ je konstanta úměrnosti.</span>
* Pokud vysvětlujeme veličiny vystupující v rovnici, není vhodné používat pomlčky, ani pomlčky následované slovesem "je". Nejjednodušší je vysvětlení pomocí slovesa "je" jako součást věty.
  * **✔ Správně (vysvětlení ve větě):** Kinetická energie je \\[E=\frac 12 mv^2,\\] kde $m$ je hmotnost tělesa a $v$ je jeho rychlost.
  * <span class="bad">**✘ Špatně (pomlčky):** Kinetická energie je \\[E=\frac 12 mv^2,\\] $m$ – je hmotnost tělesa, $v$ – rychlost tělesa.</span>
* Výčet se píše příkazy pro výčet. Není prostor pro ruční formátování a nepoužívají se tvrdé konce řádku ani odstavce. V Markdownu se výčet píše například pomocí hvězdičky, v LaTeXu pomocí prostředí typu `enumerate`, `itemize`, ..., ve Wordu pomocí odrážek.

## Znaky a symboly

Každý znak má svůj význam a nepíšeme žádný znak v kontextu, ve kterém se nepoužívá.

* Násobení se nepíše pomocí hvězdičky ani tečky na lince. Nepoužívá se nic (např. $ab$), nebo binární operátor křížek (např. $a\times b$) nebo binární operátor centrovaná tečka (např. $a\cdot b$). Hvězdička je jenom pro vstupy do počítače. Tečka za koncem věty je jiný znak než tečka pro násobení. Křížek pro násobení a písmeno x jsou také jiné znaky.
  * **✔ Správně (násobení):** Kinetická energie tělesa o hmotnosti $m$ pohybujícího se rychlostí $v$ je \\[E=\frac 12 mv^2.\\]
  * <span class="bad">**✘ Špatně (nesmí být hvězdička):** Kinetická energie tělesa o hmotnosti $m$ pohybujícího se rychlostí $v$ je \\[E=\frac 12 * m*v^2.\\]</span>
* Derivace se označuje apostrofem nebo speciálním příkazem pro derivaci. Není možné pro derivaci použít zpětný apostrof, lomítko v horním indexu a podobně.
* Značku pro implikaci není možné seskládat z rovnítka a znaku ostře větší.
* Minus je jiný znak než spojovník (-) a než pomlčka (–). Záporné číslo píšeme v matematickém režimu, tj. $-5$ jako `$-5$`. Rozsah hodnot píšeme pomlčkou, například 5–10 metrů (v LaTeXu `5--10`).
* Velikost závorek přizpůsobíme obsahu. V LaTeXu příkazy `\left(` a `\right)`.
  * **✔ Správně:** $\displaystyle \left(\frac ab\right)^2$ jako `\left(\frac ab\right)^2`
  * <span class="bad">**✘ Špatně:** $\displaystyle (\frac ab)^2$</span>
* Zlomky v textu odstavce píšeme úsporně pomocí lomítka nebo malým zlomkem (`\tfrac`), například $a/b$ nebo $\tfrac 12$. V samostatné rovnici použijeme vzdušnější zlomek (`\frac`), viz ukázka 10 v tabulce níže.

| požadovaný výstup | špatný zápis |
|--------| ------- |
| $5\cdot 2=10$    | $5.2=10$|
| $5\times 2=10$   | $5 x 2=10$  nebo $5 \text{x} 2=10$ |
|$\implies$ | $=>$|
|$1+2+3+\cdots +10$  | $1+2+3+ ... +10$|

#### Matematické značky jenom do matematických výrazů

Není vhodné vkládat matematické značky do textu. Srovnejte následující věty (z Wikipedie). Rozdíl je ve formulaci "menší než sto procent".

> ✘ Při poklesu teploty pod teplotu rosného bodu obvykle dochází ke kondenzaci vodní páry obsažené ve vzduchu, vzniká například rosa nebo mlha. Při poměrné vlhkosti $<$ 100 % je teplota rosného bodu vždy nižší než teplota vzduchu. Rozdíl mezi teplotou vzduchu a teplotou rosného bodu, který se nazývá deficit teploty rosného bodu, je tím větší, čím je menší poměrná vlhkost. 

versus

> ✔ Při poklesu teploty pod teplotu rosného bodu obvykle dochází ke kondenzaci vodní páry obsažené ve vzduchu, vzniká například rosa nebo mlha. Při poměrné vlhkosti menší než 100 % je teplota rosného bodu vždy nižší než teplota vzduchu. Rozdíl mezi teplotou vzduchu a teplotou rosného bodu, který se nazývá deficit teploty rosného bodu, je tím větší, čím je menší poměrná vlhkost. 

Druhá formulace je srozumitelná, první formulace působí dojmem, že se někde ztratila polovina nerovnice.

## Obecné zásady psaní

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

#### Text a vzhled textu se zapisují na jiných místech

Nadpis označíme jako nadpis a neměníme velikost písma ani font nebo
řez. Vzhled nadpisu potom vyřešíme v šabloně (šablona pro Word, css
styl pro html, hlavička dokumentu pro LaTeX). Totéž v jiných podobných
případech. Výhoda je, že změna šablony se projeví v celém
dokumentu. Při ručním formátování se musí vše procházet a opravovat.

## Komentované ukázky chybných zápisů

|Číslo|✘ Špatně|✔ Správně|Vysvětlení|
|-|----|----|----|
|1|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336*l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je zápis násobení. Násobení zapisujeme hvězdičkou jenom ve vstupech pro počítač. Pro texty určené lidem **hvězdičku nepoužíváme**. Nepíšeme buď nic, nebo `\times` nebo `\cdot`, tj. $1.336\times l^{0.67}$ nebo $1.336\cdot l^{0.67}$.|
|2|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 \cdot\mathrm l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336\cdot l^{0.67}.\\]|Špatně je font pro proměnnou označující délku kroku. Matematické proměnné zapisujeme matematickou kurzívou. To je defaultní font v matematickém prostředí, tedy v praxi to znamená, že **nic ručně nepřepínáme**, pokud si opravdu nejsme jisti, že to je potřeba (jako například u jednotek).|
|3|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je chybějící konec věty. Na konci věty píšeme **tečku**. (Pozor, toto pravidlo nemusí platit v anglickém textu, tam záleží na typografovi publikace.)|
|4|Jednotka derivace rychlosti dinosaura podle délky kroku je $s^{-1}.$|Jednotka derivace rychlosti dinosaura podle délky kroku je $\mathrm s^{-1}.$|Špatně je font pro zápis jednotky. Úmysl byl zapsat převrácenou hodnotu sekundy, ale zapsána je převrácená hodnota dráhy. Fyzikální jednotky se nepíšou matematickou kurzívou, ta je vyhrazena pro proměnné. Přepínáme do **textového fontu** příkazem `\mathrm`.| 
|5|Jednotka derivace rychlosti dinosaura podle délky kroku je \\[\mathrm s^{-1}.\\]|Jednotka derivace rychlosti dinosaura podle délky kroku je $\mathrm s^{-1}.$|Špatně je umístění vzorce s jednotkou na samostatný řádek. Velmi krátké vzorce si umístění na **samostatný řádek** zaslouží jenom výjimečně. Například pokud vzorec potřebujeme očíslovat. Krátké matematické výrazy píšeme do textu odstavce.| 
|6|Derivace rychlosti dinosaura podle délky kroku je: \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Derivace rychlosti dinosaura podle délky kroku je \\[\frac{\mathrm dv}{\mathrm dl}=1.336 l^{0.67}.\\]|Špatně je použití dvojtečky. Snažíme se o co nejhladší začlenění matematických výrazů do textu. Kdyby místo vzorce bylo slovo, tak taky žádnou **dvojtečku nepoužíváme**. Proto není potřeba ji psát ani v situaci, kdy je místo slova vzorec. Co není potřeba psát a nepřispívá k čitelnosti, to ani nepíšeme. (Podobně jako tečka za větou, pravidlo nemusí platit v jiných jazycích a při speciálních požadavcích typografa.)|
|7|Z Buckinghamova II teorému vyplývá pro kužel s daným úhlem u vrcholu vztah mezi objemem $V$ a výškou $h$ ve tvaru \\[V = kh^3.\\]|Pro kužel s daným úhlem u vrcholu je objem $V$ úměrný třetí mocnině výšky $h$, tj. platí \\[V = kh^3\\] pro vhodnou konstantu $k$.|Špatně je název věty, v názvu není římská dvojka, ale velké řecké písmeno "pí". Obecně platí, že **ve vlastních textech používáme jenom takové informace, o kterých jsme stoprocentně přesvědčeni, že jsou správně.** Pokud si například nejsme jisti názvem věty, v naprosté většině textů je možné se mu vyhnout.|
|8|$k$ je konstanta úměrnosti.|Veličina $k$ je konstanta úměrnosti.|Není vhodné začínat větu matematickým výrazem. Vždy je možné použít formulaci, kdy **věta začíná běžným slovem**. Poté je možné toto slovo napsat s velkým písmenem na začátku a je zcela zřejmé, že zde začíná nová věta.|
|9|Z Pythagorovy věty \\[a^2+b^2=c^2\\] $\qquad$je možné vypočítat délku odvěsny pomocí přepony a druhé odvěsny.|Z Pythagorovy věty \\[a^2+b^2=c^2\\] je možné vypočítat délku odvěsny pomocí přepony a druhé odvěsny.|V ukázce je pod rovnicí další odstavec, obvykle se to prozradí odsazením prvního řádku o odstavcovou zarážku. Toto se vyskytuje u uživatelů MS Word, kteří rovnici centrují tak, že ji dají do samostatného odstavce a ten vycentrují jako klasický text. Správný postup je použít pravé tlačítko myši u rovnice a zvolit z menu položku "Změnit na samostatný".|
|10|Odporová síla je dána vztahem \\[F=\tfrac 12 C\rho v^2.\\]|Odporová síla je dána vztahem \\[F=\frac 12 C\rho v^2.\\]|Zlomek je napsán úsporným fontem určeným do textu nebo tam, kde je málo místa. Pro samostatnou rovnici má být vzdušnější. V MS Word tato varianta naskočí automaticky po volbě "Změnit na samostatný".| 

## Kontrolní seznam před odevzdáním

* [ ] Všechny proměnné (i jednotlivá písmena v textu) jsou zapsány jako matematika.
* [ ] Jednotky, funkce, diferenciál $\mathrm d$, $\mathrm e$ a $\mathrm i$ jsou textovým fontem.
* [ ] Za každou rovnicí je interpunkce podle pravidel pravopisu (čárka, tečka).
* [ ] Uvnitř věty nekončí odstavec, ani kolem rovnic.
* [ ] Žádná věta nezačíná vzorcem nebo číslem.
* [ ] Před rovnicemi nejsou zbytečné dvojtečky.
* [ ] Násobení není zapsáno hvězdičkou, tečkou na lince ani písmenem x.
* [ ] Číslované jsou jen rovnice, na které se odkazuji.
* [ ] Označení veličin je stejné v celém textu.
* [ ] Vzhled je řešen šablonou, ne ručním formátováním.
