.. index::
    single: Formát
    see: Formát souboru; Formát

Otevřené formáty, webové služby a distribuce otevřených geodat
==============================================================

V této kapitole se zaměříme na vhodné datové formáty pro otevřená geodata.
Zmíníme populární datové formáty, které jsou ale často pro tento účel nevhodné.
Podrobněji zhodnotíme dostupné webové služby jako vhodný a široce využívaný
způsob distribuce geodat.

**Formát** určuje význam dat v elektronickém souboru. Formát je způsob, jakým jsou
data v souboru uložena. Formáty jsou často navrženy specificky pro
určitý typ dat. V základu lze formáty rozdělit na binární (z pohledu člověka se
jedná o souvislý tok hodnot 0 a 1) a textové (které jsou pro člověka poměrně jednoduše
čitelné). Příkladem binárního formátu může být JPEG, speciálně navržený k
ukládání obrazových dat. Příkladem textového formátu může být formát JSON či XML,
určené k popisu a ukládání libovolných stromových datových struktur.

**Webové služby** jsou softwarové systémy umožňující interakci dvou strojů na
počítačové síti. Počítače mezi sebou komunikují pomocí srojově spracovatelného *formátu*
zpráv. Webové služby ke své komunikaci využívají protokolu HTTP (Hypertext
Transfare Protocol), o který je opřen World Wide Web (WWW -- odtud *webové
služby*). Jeden z počítačů ve vzájemné komunikaci vždy
vystupuje jako *klient* (požaduje po serveru splnění nějakého úkolu), druhý jako
server (vyřizuje žádost a posílá klientovi odpověď). Výsledkem odpovědi může
například být i obrázek v patřičném souborovém *formátu*, jako je JPEG.

.. index:: 
    single: Formáty
    see: Otevřené formáty; Formáty

Otevřené formáty
----------------
Formáty pro publikování otevřených geodat by měly být zejména *otevřené* -- ať už
proprietární, tj. spravované konkrétní firmou anebo standardizované
`konsorciem OGC <http://www.opengeospatial.org/>`_ či technickou
normou ISO. Otevřený formát je takový formát, ke kterému existuje
volně dostupná dokumentace a zároveň jeho licence umožňuje jeho volné
využívání. V ideálním případě je vyvíjen nezávislou mezinárodní
standardizační organizací a není navázán přímo na žádný privátní
subjekt.

Z dlouhodobého hlediska je výhodnější využívat formáty otevřené a
standardizované, než proprietární (jakkoliv mohou být široce rozšířené mezi
uživately a jimi používanými programy), zejména protože:

* Stává se, že firma (autor proprietárního formátu a držitel licenčních práv k
  němu) svůj formát změní, případné programové nástroje třetích stran
  pak reagují se zpožděním, pokud vůbec 
* Uživatelé jsou nuceni používat konkrétní software, což nemusí být pro některé z
  nich z technických, licenčních nebo finančních důvodů akceptovatelné
* Celý systém se stává závislý na jedné firmě či dodavateli softwarového řešení,
  je nepřenositelný a v budoucnu jen těžko rozšiřitelný

Z pohledu výše zmíněné :ref:`pětihvězdičkové konvence
<pet-hvezdicek>`, můžeme pro geodata uvést následující příklady
vhodných datových formátů:

.. tabularcolumns:: |p{.1\textwidth}|p{.8\textwidth}|

+-------+--------------------------------------------------------------------------------+
| ★     | Tisknutelná mapa je uložena ve formátu PDF nebo v rastrovém formátu jako       |
|       | obrázek, například JPEG, GIF či PNG                                            |
+-------+--------------------------------------------------------------------------------+
| ★★    | Vektorová data jsou uložena v uzavřeném proprietárním formátu, například DWG   |
|       | firmy Autodesk                                                                 |
+-------+--------------------------------------------------------------------------------+
| ★★★   | Vektorová data jsou uložena ve formátu Esri Shapefile; který je sice           |
|       | proprietární, ale je otevřený; nebo jako OGC GML, což je otevřený standard a   |
|       | zároveň technická norma ISO                                                    |
+-------+--------------------------------------------------------------------------------+
| ★★★★  | Data jsou opatřena metadaty a jednotlivé datové sady jsou jimi navzájem        |
|       | provázány. Předpokládá se existence metadatového katalogu, založeného na       |
|       | standardu OGC Catalog Service for Web (CSW), ve kterém lze data a služby       |
|       | vyhledávat                                                                     |
+-------+--------------------------------------------------------------------------------+
| ★★★★★ | Jednotlivé geoprvky datové sady jsou navzájem provázány pomocí unikátních      |
|       | identifikátorů                                                                 |
+-------+--------------------------------------------------------------------------------+

Výsledkem otevření dat by mělo být jejich zpřístupnění a tím jejich snadné a
efektivní využití. Z tohoto důvodu je nejprve nutné identifikovat potenciální
uživatele a jejich typický pracovní postup tak, aby zvolené řešení pro otevření
dat bylo co možná nejvhodnější. Hlavní skupiny uživatelů z pohledu IPR Praha
budou pravděpodobně pracovníci ve stavebnictví, využívající některý ze systémů
CAD a uživatelé Směrnice INSPIRE jako současného legislativního a technického
rámce pro některý z geografických informačních systémů (GIS).

Kromě souvisejících zákonů a nařízení je pro otevírání geodat relevantní zejména
evropská směrnice INSPIRE [ref26]_ ze dne 25. dubna 2007, která vstoupila v platnost
15. května 2007. Tato směrnice tvoří evropský legislativní rámec potřebný k
vybudování evropské infrastruktury prostorových informací zejména k podpoře
environmentálních politik a politik, které životní prostředí ovlivňují.
Hlavním cílem směrnice INSPIRE je poskytnout množství kvalitních a
standardizovaných prostorových informací. Směrnice byla transponována do
národní legislativy České republiky novelou zákona č. 380/2009 Sb. [ref27]_.  

Formáty souborů pro distribuci otevřených geodat
------------------------------------------------

Pro ukládání, zpracování a výměnu geografických dat existuje velké množství
formátů. Z hlediska otevřených geodat se prozatím můžeme omezit na formáty
rastrové a vektorové. 

.. index::
    single: Rastry
    pair: GeoTIFF; TIFF
    single: JPEG
    single: PNG
    single: GIF

Rastrová data
~~~~~~~~~~~~~

**GeoTIFF**

Formát GeoTIFF [ref16]_ je typickým a nejrozšířenějším otevřeným formátem pro
distribuci rastrových geografických dat. Tento formát umožňuje uložit nejen
rastrová data, ale také všechny typy gridových dat. Informace o souřadnicovém
systému, souřadnicovém umístění a další popisné informace jsou uloženy přímo v
hlavičce  souboru. Při uložení dat do tohoto formátu nedochází při vhodné volbě
komprese k nevratné ztrátě informace.

**JPEG**

Formát JPEG [ref17]_ je kompresní určený k uložení rastrových souborů. Jeho výhodou
je úspora místa a tudíž i menší nároky na datový přenos. Jeho nevýhodou je to,
že komprese je ztrátová -- formát tedy není vhodný pro použití v GIS, neboť data
jsou nenávratně poškozena a jsou tak pro další zpracování nepoužitelná. Na
druhou stranu, pokud obrázek JPEG je použit pouze jako podkladová vrstva (např.
u leteckých snímků, u kterých se nepředpokládá žádné jiné využití), lze tak
snížit nároky na datový tok. JPEG je nejčastěji výsledkem volání webové
prohlížecí služby. Pokud je šířen samostatně, je potřeba jej opatřit metadatovým
souborem se souř. umístěním (koncovka .jpw).

**PNG**

Formát PNG [ref76]_ byl vytvářen jako nástupce formátu JPEG kvůli softwarovým
patentům, použitým právě ve formátech JPEG a GIF. Některá data komprimuje lépe.
Komprese nepoškozuje ostré hrany. Z tohoto důvodu se tento formát využívá pro
topografické podkladové mapy v prohlížecích službách OGC WMS a WMTS. Komprese
fotografií s množstvím gradientů již není tak efektivní. Pro uložení geodat je
tento formát opět nevhodný, kvůli limitu barevné škály, částečně ztrátové
kompresi dat a omezení na 3 barevné kanály + průhlednost. Soubory ve formátu PNG
jsou nejčastěji výsledkem volání webové prohlížecí služby. Pokud jsou šířeny
samostatně, je potřeba jej opatřit metadatovým souborem se souř. umístěním
(koncovka .pnw).

**Ostatní rastrové formáty**

Ostatní formáty pro uložení rastrových dat nedosáhly takového rozšíření jako
formát GeoTIFF. Řada z nich je proprietárních a jsou používany často pouze
oborově (MrSID, BMP, ArcSDE Raster, ...).
Za zmínku stojí formát GIF, který měl své využití v minulosti hlavně
mezi webovými mapovými aplikacemi. Formát GIF disponuje omezenou barevnou
škálou, pro geodata je nevhodný (nejedná-li se o data binární nebo s rozsahem
hodnot 0-255).  Z tohoto důvodu byl GIF nahrazen zmíněným modernějším formátem
PNG. Pro GIF platí to samé, co pro soubory JPEG a PNG - pokud již obsahuje
geodata a je šířen samostatně - tedy není výsledkem volání webové služby, musí u
něj být přítomen metadatový soubor .gfw.

.. index::
    single: Vektory
    pair: SHP; Esri Shapefile
    single: GML
    single: KML
    tripple: JSON; GeoJSON; TopoJSON
    single: SpatiaLite
    single: GeoPackage

Vektorová data
~~~~~~~~~~~~~~

**OGC Geospatial Markup Language**

OGC GML [ref19]_ jako otevřený standard je perspektivním formátem pro přenos
vektorových dat. Jedná se o jednosouborový textový formát založený na
značkovacím jazyce XML, je proto interpretovatelný i bez speciálního software.
Kromě standardizace na úrovni OGC je definován technickou normou ISO 19136.
Vzhledem k tomu je podporován většinou moderních GIS nástrojů. GML je také
předepsaný technickými dokumenty INSPIRE a výchozím formátem služby OGC WFS.

GML se používá jako univerzální formát pro data, která mohou mít i
komplikovanější stromovou strukturu. Díky tomu, že je postaven na XML, je jeho
strojové zpracování jednoduché i běžnými systémy, například pomocí transformace
XSLT.

**OGC Keyhole Markup Language**

Další možností je formát OGC KML, který je určen především pro vizualizaci
jednotlivých geoprvků. Formát byl původně vyvinut firmou Google a je také
postavený na jazyce XML. Data v souborech KML, na rozdíl od GML, umožňují použít
pouze souřadnicový systém WGS84.

KML podporují samozřejmě produkty firmy Google, ale i řada služeb a programů
třetích stran. Bývá často podporován moderními GPS přijímači. Často býval
nasazován na webových aplikacích, protože je v porovnání s GML menší a obsahuje
zmíněnou informaci o vizualizaci jednotlivých geoprvků. Ačkoliv byl v době před
cca 3 lety tento formát populární, dnes je často nahrazován formátem GeoJSON.

**Formáty odvozené z datového formátu JSON**

Populárním formátem se v poslední době stává formát GeoJSON [ref68]_, který je
založen na formátu JSON. Své uplatnění má především mezi webovými technologiemi.
Oproti formátům odvozených z XML (GML, KML) má kratší zápis, což  je výhodné při
přenosech v prostředí Internetu. Stejně jako při využití formátů odvozených z
XML, je i zde je možné zabezpečit správnost struktury dat to pomocí schémat.

Formát JSON je velice přívětivý k netypovým programovacím jazykům, opět je
srozumitelný prostým lidským okem. Souřadnicový systém zde není jak
specifikovat, předpokládá se, že se jedná o WGS84. Data lze libovolným způsobem
zanořovat a větvit.

Formát GeoJSON je využíván u webových služeb pro svůj malý objem a jednoduchost.
Je méně náročný na zpracování, což je vhodné zejména u webových prohlížečů. U
uživatelů mimo svět GIS je oblíbený, protože jeho strukturu je možné rychle
pochopit a připravit vlastní parser.

Dalším formátem odvozeným z formátu JSON, který ale zatím nenabyl takové
popularity jako GeoJSON je formát `TopoJSON
<https://github.com/mbostock/topojson>`_. Hlavním úkolwm formátu TopoJSON je
minimalizace datového toku mezi webovým serverem i klientem. Formát je částečně
ztrátový, neboť souřadnice bodů a lomových bodů jsou zapisovány v relativní
poloze od danného počátku a v celých číslech (ztrácí se přesnost). K úspoře
datové velikosti vede také fakt, že např. hranice polygonů jsou uloženy pro dvě
sousedící plochy pouze jednou (formát je tedy topologický).

Formát TopoJSON je velice slibný a v budoucnu nebude jediný (firma MabBox přišla
v poslední době také se svým vlastním formátem progeodata postaveným nad
zápisem JSON). V tuto chvíli naráží zejména na nedostatečnou podporu v
softwarech. Není ani vhodný jako obecný formát pro výměnu dat mezi systémy, je
ale navržen s ohledem na optimalizaci aplikací ve webovém prostředí a tam má
taky své místo.

**Geodatabáze SpatialLite**

Geodatabáze SpatiaLite je postavená na souborové Open Source databázi SQLite.
SQLite je přítomna v řadě zařízení či programech, interně ji využívá např.
prohlížeč Firefox. SpatiaLite je její prostorové rozšíření, podobně jako PostGIS
prodatabázi PostgreSQL. SpatialLite umožňuje uložit a pracovat s geodaty v
prostředí SQL databáze, která je ovšem uložena v jednom jednoduše přenositelném
souboru.

SpatiaLite je vhodný formát na lokální uložení dat, ale v praxi se pro výměnu
dat příliš nepoužívá.

**Komplexní formát OGC GeoPackage**

Moderním nástupcem výše zmiňovaných rastrových, ale především vektorových
formátů je standard OGC GeoPackage [ref39]_. Tento formát umožňuje uložit libovolná
vektorová data spolu s daty rastrovými, ať už ve formě dlaždic, nebo souborů ve
formátu GeoTIFF do prostředí databáze SQLite. Poskytuje tak jednoduché rozhraní
jazyka SQL pro práci s daty [#geopackage]_. Vektorová data jsou uložena dle specifikace OGC
Simple Features for SQL [ref40]_. Maximální velikost databázového souboru je 140 TB,
což je pro praktické použití většinou dostačující. Data v jedné datové vrstvě,
tedy  databázové tabulce, mohou mít různé typy geometrií. Řada GIS nástrojů již
podporu pro OGC GeoPackage nabízí, včetně Open Source knihovny GDAL od verze
1.11 či proprietárního prostředí Esri ArcGIS od verze 10.2.1.

OGC GeoPackage se zatím v praxi příliš nepoužívá. Nicméně vzhledem k tomu, že se
jedná o standard OGC umožňující  práci s opravdu komplexními datovými
strukturami, jsme toho názoru, že by se tento formát měl pro otevřená geodata
využívat a to i přesto, že podpora tohoto formátu není v běžných programech mimo
svět GIS příliš rozšířena.

**Esri Shapefile**

Esri Shapefile (Shapefile, SHP) je v praxi již dlouhou dobu nejpoužívanějším
formátem pro výměnu vektorových geodat [ref18]_. Bohužel je tento formát v
dnešní době již poněkud omezující, zejména z důvodů zmíněných níže.
Stále je ale používán pro menší datové soubory a jednoduché datové sady bez
komplikovaných vazeb mezi objekty a tabulkami, protože je to formát jednoduchý a
poskytuje jistotu kompatibility mezi různými softwarovými platformami.

Mezi slabá místa formátu patří zejména to, že data nejsou uložena v jednom
souboru, ale hned ve trojici (shp+shx+dbf), různé softwarové produkty si navíc
přidávají vlastní metadatové soubory, které nejsou součástí specifikace tohoto
formátu [#shp]_. Názvy atributů jsou omezeny pouze na deset znaků. Data
neobsahují informaci o znakové sadě, což vede k problémům při automatické
konverzi dat a používání na více operačních systémech. Velikost souborů je
maximálně 2GB.  Neumožňuje ukládat topologické informace o vzájemných vztazích
mezi geoprvky.  Každý soubor `shp` umožňuje ukládat pouze jeden typ geometrie
(bod, linie, polygon) a neumožňuje uložit stromovou strukturu dat.

.. index::
    single: Distribuce geodat

Distribuce otevřených geodat
----------------------------

Na způsob distribuce libovolných dat má vliv mnoho faktorů, zejména životní
cyklus poskytovaných dat a typ uživatele, který je bude využívat.

S ohledem na životní cyklus dat je třeba rozlišovat mezi statickými daty a těmi,
které se průběžně mění (dynamická data). Příkladem statických dat jsou výstupy
analýz a data popisující konkrétní stav. Data, která se v čase mění můžeme potom
dále dělit na dva základní okruhy. Do prvního náleží taková data, která popisují
v reálném čase se měnící jev, to může být například znečištění, demografická
data atd. Druhým typem jsou data, která nepopisují proměnlivý jev, ale jsou
průběžně nebo nárazově zpřesňována. Takovými daty může být například digitální
model reliéfu.

Typ uživatele je druhým z faktorů, který je vhodné mít na paměti při volbě
způsobu distribuce geodat. S určitou mírou zjednodušení lze konstatovat, že čím
jsou data komplexnější, tím obtížnější je jejich uchopení na straně příjemce.
Příkladem jsou data, která není možné zredukovat na jednu databázovou tabulku,
aniž by došlo k jejich nevratné degradaci. K využití dat v komplexnější
struktuře je nutné mít hlubší znalosti než pouhé přidání vrstvy do projektu v
desktopovém GIS. Uživatel navíc může k takto publikovaným datům přistupovat
různými způsoby.

V této kapitloe rozebíráme vhodné způsoby distribuce otevřených geodat, zejména
pomocí webových *služeb OGC* a také pomocí publikačního standardu *Atom*.
Nakonec se zmíníme o alternativní možnosti publikace geodat pomocí služby *Github*.


.. index::
    single: Distribuce geodat

Specifika distribuce geodat
~~~~~~~~~~~~~~~~~~~~~~~~~~~

V současnosti je kladen velký důraz na webová řešení a mobilní aplikace, které
mají specifické požadavky. Je zde velice důležitá rychlost přenosu dat. Zejména
u dat využitelných pouze pro zobrazování je proto vhodné využívat metody
modelové generalizace a posílat spojením mezi serverem a klientem co nejmenší
množství dat.  Pro podporu těchto aplikací byly vyvinuty speciální formáty dat,
založené na specifikacích JSON, jako jsou GeoJSON a TopoJSON, které jsou pro
webové aplikace obzvlášť výhodné a v současné době velice populární. U mobilních
aplikací se často pracuje s lokalizací pomocí Global Positioning System (GPS).
Pro taková řešení je vhodné umožnit stahování dat přímo v souřadnicovém systému
WGS84.

Základním způsobem distribuce geodat by měly být *webové služby OGC*. V tomto
případě získává uživatel vždy nejaktuálnější data. Nevýhodou je ovšem zátěž na
straně infrastruktury poskytovatele, kterou není možné vždy předvídat, konzument
navíc očekává garanci jejich dostupnosti. Zátěž serverů je potřeba průběžně
sledovat a adekvátně na ni reagovat. V tomto směru může být cestou pro
distribuci otevřených geodat využití cloudového řešení na pronajatých sdílených
serverech, kde je výkon dynamicky zvyšován podle potřeby a cena potom odpovídá
využití. K tomu je však potřeba překonat určitou psychologickou bariéru, jelikož
data a infrastruktura zdánlivě nejsou pod kontrolou jako v případě, že použijete
řešení vlastní.

Pro uživatele je nejnáročnějším postupem získání dat tzv. strojové vytěžování
(harvesting) poskytovaných dat a budování databáze na svém hardware. U dat,
která jsou průběžně aktualizována, je v těchto případech nutné umožnit jak
získávání stavových dat (tj. dat platných k určitému datu), tak změnových vět
formou předgenerovaných souborů. Režim výdeje je vhodné nastavit s ohledem na
objem změn. Toto řešení často vede ke snížení zátěže na infrastrukturu
poskytovatele.

Specifickou oblastí u výdeje dat je poskytování dat agregovaných (znepřesněných
nebo bez některých atributů). Obvyklým důvodem agregace [#agregace]_ bývají citlivé údaje
(osobní údaje, data vlastněná třetími stranami).

Výdejní systém, má-li být efektivní a funkční, musí kopírovat charakter dat, nad
kterými je postaven. Výdejní systém není správné vyvíjet nezávisle na datech,
které má vydávat. Tento (výdejní) systém by měl ideálně "růst" spolu s daty, pro
které je vytvářený.


.. index::
    single: INSPIRE
    single: Implementační pravidla INSPIRE
    single: ATOM

Implementační pravidla INSPIRE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Jedním z osvědčených způsobů distribuce geodat v Evropské unii je využití
prohlížecích, stahovacích služeb a vyhledávacích služeb podle směrnice INSPIRE,
která se také opírá o standardy konsorcia OGC. O tom, že směrnici INSPIRE, resp.
technické dokumenty s ní svázané, lze považovat za “best-practice” svědčí i to,
že podobné postupy se prosazují i jinde ve světě, například na Novém Zélandu
[ref46]_. Popis implementace jednotlivých částí směrnice je obsažen v tzv.
implementačních pravidlech. Na publikaci vektorových a rastrových dat se
vztahuje technický průvodce [ref28]_. 

Technický průvodce pro implementaci *Stahovací služby INSPIRE* se dotýká právě
problematiky velkých datových sad. Nabízí dvě možnosti implementace této služby:

* *Předgenerované soubory* s datovou sadou a jejich distribuce prostřednictvím
  dokumentu ve formátu ATOM -- ovšem bez možnosti jejich dotazování či
  výběru části dat prostřednictvím serveru.
* Webové služby OGC WFS a WCS (tak zvané *datové sady s přímým přístupem*). 
  Ty rozšiřují možnosti předgenerovaných datových sad o možnost filtrovat
  požadovaná data již na straně serveru. 

V obou případech je k dispozici tzv. Get Download Service Metadata Request. V
prvním případě seznam odkazů ve formátu Atom (viz kapitola :ref:`atom`), v
druhém případě pomocí WFS nebo WCS GetCapabilities.

Implementační pravidla směrnice INSPIRE definují také požadavky na dostupnost
služeb, jejich kapacitu a rychlost odezvy.  Praxe ukazuje, že požadavky
definované v technických specifikacích INSPIRE jsou velice vágní, nedostatečně
specifikované a v praxi dokonce podhodnocené (např. požadovaná dostupnost služby
99% znamená, že služba může být nedostupná 3.65 dne v roce!). Jak bylo napsáno
výše, zátěž je potřeba průběžně sledovat a adekvátně na ni reagovat.

Otevřené webové služby - OGC OWS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Jako nejpřirozenější cestou distribuce otevřených geodat se jeví využít otevřené
webové standardy OGC Open Web Services (OWS). Nejpoužívanějšími službami jsou
OGC WMS, WFS a WCS. Existují však i jiné standardy, mající opodstatnění v
některých případech použití. Standardy OGC jsou postaveny nejčastěji na
komunikaci mezi serverem a klientem prostřednictvím zpráv ve formátu XML. Tyto
standardy mají dobrou podporu ve většině používaných programů. OGC služby jsou
použité i v technických normách směrnice INSPIRE. 

V této části zmíníme pouze nejčastěji používané standardy, které pokrývají
většinu případů použití:

* OGC Web Map Service
* OGC Web Map Tiled Service
* OGC Web Feature Service
* OGC Web Coverage Service
* OGC Sensor Observation Service

**OGC Web Map Service (OGC WMS)**

OGC Web Map Service [ref20]_ je standard, pomocí kterého může klient požádat o
mapový obraz ve formě rastrového souboru. Server jej na základě klientských
požadavků vytvoří a klientovi odešle. Klient musí specifikovat obsah obrázku
(zobrazené vrstvy), souřadnicový systém, hraniční souřadnice, velikost, formát
obrázku a další možné detaily. Server odešle opravdu “pouze” obrázek a nikoliv
vlastní data. To lze s výhodou využít pro případ, že chce uživatelům zpřístupnit
některé data pouze k nahlédnutí, ale nechce nebo nemůže zpřístupnit data jako
taková. Standardním formátem výstupu je obrázek ve formátech PNG nebo JPEG podle charakteru dat.

**OGC Web Map Tiled Service (OGC WMTS)**

Pokud se data v čase příliš nemění (například letecké snímky, obecně podkladové
mapy), lze si na straně serveru připravit předgenerované dlaždice (obrázky o
pravidelné velikosti, většinou 256x256 pixelů) do vyrovnávací paměti pro určitá
měřítka a v určitém rozsahu (*cache*).  Tyto dlaždice pak lze zpřístupnit podle
standardu OGC WMTS [ref23]_ (nebo i WMS). Výhodou je rychlé odbavení příchozího
požadavku a nižší zátěž IT infrastruktury. Nevýhodou je, že dlaždice musí být
omezeny pro určitá měřítka. Obsah je statický (v čase se nemění, datové vrstvy
vykreslené v obrázku jsou stále stejné). Takto vytvořenou databázi dlaždic je
potřeba udržovat, pravidelně aktualizovat a mít pro ni dostatečně velkou
diskovou kapacitu.  Standardním formátem výstupu je obrázek ve formátech PNG
nebo JPEG podle charakteru dat.

Jako vhodná sada měřítek spolu s výchozím “počátkem” dlaždic se ukazuje řada
dlouhodobě používaná servery ČÚZK, který pro souřadnicový systém S-JTSK
(EPSG:5514, dříve EPSG:2065 či ESRI:102067) vyvinul vlastní řadu měřítek
[ref24]_. Pro globální souřadnicové systémy (jako je např. “Spherical Mercator”
EPSG:3857) se doporučuje používat měřítkovou řadu vyvinutou firmou Google.

**OGC Web Feature Service (OGC WFS)**

OGC Web Feature Service [ref21]_ slouží k distribuci vektorových dat. Standard WFS
2.0.0 umožňuje také spouštět některé analytické operace přímo na serveru,
jsou-li na něm podporovány. WFS dále podporuje filtrování pouze požadovaných
geoprvků (vzhledů jevů,  features), není tak potřeba stahovat celou datovou
sadu. Pro větší objemy dat je možné použít možnost stránkování odpovědi, tj.
nemusí být stahována všechna data najednou v jedné odpovědi. Pomocí WFS může
server vrátit data v libovolném formátu, který podporují knihovny pracující na
pozadí (i Esri Shapefile, GeoJSON, …), standardní bývá formát OGC GML.
                                     
**OGC Web Coverage Service (OGC WCS)**

OGC Web Coverage Service [ref22]_ slouží k distribuci rastrových dat. Tento standard
je vhodný zejména tam, kde chceme uživatelů nabídnout ke stažení velká rastrová
data, která mohou být i multispektrální, či mohou obsahovat více rozměrů.
Standardním formátem výstupních dat bývá GeoTIFF.

**OGC Sensor Observation Service (OGC SOS)**

Služba OGC Sensor Observation Service [ref72]_ je vhodná pro zpřístupnění měření ze
senzorů a senzorových sítí, stejně jako pro jejich popis. Senzory většinou
publikují několik měření k danému místu a v daném čase. Poloha senzoru může být
statická, ale může se i v čase měnit. Senzory mohou měřit různé veličiny a v
různých časových úsecích.

.. index::
    single: Atom
    single: FTP

.. _atom:

Předgenerované soubory a formát Atom
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Pro datové sady větších objemů je vhodné předgenerovat jejich obsah do cílových
vektorových formátů a postavit kolem nich architekturu, která v nich umožní
efektivně vyhledávat. Jako jeden z vhodných nástrojů může být např. formát Atom
[ref25]_. Tento formát je využíván i v dalších technologických standardech, jako je
například OGC OWS Context [ref38]_. V principu jde o XML dokument, který obsahuje
odkazy a základní metadata na dostupné datové sady nebo soubory.

Tento způsob se blíží populárnímu a velice jednoduchému přístupu "vystavit
soubory na FTP server". To se s formátem Atom nevylučuje - Atom slouží pouze
jako metadatový dokument, ze kterého lze rychle vyčíst referenci k cílovým
souborům.

Soubor ve formátu Atom je webový standard pro publikování syndikovaného obsahu.
Syndikovaný obsah je takový obsah, který na webu již může být publikován,
souborem Atom se mu ale zpětně přidají některá metadata a tím se jednodušeni
popíše pro automatické zpracování. Atom má nahradit starší (proprietární a
stále populární formát RSS) a je původně určen pro webové stránky. Nicméně jeho
využít pro data se nabízí.

Soubor Atom jednak obsahuje hlavičku, která identifikuje vlastní zdroj a autora
a jednak seznam "záznamů", také s jednoznačnou identifikací a hlavně s vlastním
obsahem nebo odkazem na tento obsah.

Příklad formátu atom je uveden v :ref:`atom-priloha`.


.. index::
    single: GitHub

Služby GitHub
~~~~~~~~~~~~~

Služba GitHub [ref41]_ je webové rozhraní k systému pro správu verzí Git, který byl
původně napsán za účelem správy a udržby zdrojového kódu jádra operačního
systému GNU/Linux. Od  roku 2014 je možné do této služby nahrávat i geografická
data v některých z podporovaných formátů GeoJSON a TopoJSON. Tyto soubory jsou
přímo vizualizovány v jednoduché mapové aplikaci. Podle různých údajů se zdá, že
limit pro velikost vstupního souboru, má-li být zobrazen v mapové prohlížečce,
je v současnosti někde okolo 4.5 MB, záleží ale také na struktuře vstupního
souboru  [ref42]_. U jednodušších struktur může být limit až někde u 10 MB
(maximální velikost souboru na serverech GitHub je cca 100 MB). Pokud je datový
soubor příliš veliký, tak není zobrazen. Jeho praktickou dostupnost to
samozřejmě nijak neovlivní.

Takto jednoduše publikovaná data lze stáhnout opět v jednom z podporovaných
formátů. Výhoda tohoto přístupu je mimo jiné v tom, že poskytovateli dat zcela
odpadá starost o IT infrastrukturu. O tu se stará třetí strana - v tomto případě
GitHub. Uživatelé navíc  získají efektivní nástroj pro verzování dat v čase.
Pokud by byla služba GitHub v budoucnu uzavřena anebo by se změnila výrazně její
obchodní politika, nejednalo by se o tak zásadní problém. Systém Git je
decentralizovaný, každý uživatel má u sebe lokální kopii celé datové sady včetně
veškeré historie. Vzhledem k tomu, že je systém pro správu verzí Git vyvíjen
jako Open Source, tak by bylo možné případný přechod na jinou formu distribuce
ze služby GitHub realizovat bez větších problémů.

Některé menší obce a samosprávy již se službou GitHub experimentují [ref43, 44]_.
Do prostředí GitHub lze nahrát i dlaždicovaná rastrová data a odkazovat se na ně
formou zápisu identifikátoru URL podle standardu OGC Tile Map Service (TMS).
Podle zkušeností uživatelů se jeví tato služba jako dostatečně rychlá. 

Tento přístup k publikování geodat je vhodnější pro menší města bez vlastního IT
oddělení. Nicméně některé koncepty tohoto přístupu (správa verzí, distribuce,
náhled, atd.) jsou aplikovatelné i na tuto případovou studii. Některá větší
města již se službou GitHub experimentují, jak dokládá například účet města
Chicago [ref57]_.

Doporučení volby formátů a způsobů distribuce
---------------------------------------------

Doporučení formátu souborů
~~~~~~~~~~~~~~~~~~~~~~~~~~

Nelze jednoduše doporučit jeden či dva formáty vhodné pro všechny uživatele a
datové sady. Vždy je potřeba zvážit charakter dat a převládající způsob jejich
použití. 

Pro předgenerované soubory vektorových dat doporučujeme, v dlohodobém horizontu
formát OGC GeoPackage. V krátkodobém horizontu lze použít i formát ESRI
Shapefile nebo OGC GML, z toho důvodu, že formát GeoPackage není zatím příliš
rozšířen. 

Pro publikování formou prohlížecích webových služeb (OGC WMS, WMTS) je vhodné
volit  v závislosti na charakteru dat formáty PNG a JPEG;

V případě stahovacích služeb doporučujeme pro vektorová data formát OGC GML (ISO
19136) a pro rastrová data potom GeoTIFF či JPEG, podle jejich charakteru.  


Doporučený způsob distribuce otevřených geodat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Jako primární doporučujeme využít standardy OGC OWS, zejména Web Map Service
(WMS), Web Feature Service (WFS) a Web Coverage service (WCS).

Kde to z důvodu velikosti datových sad nebo pro technická omezení na straně
poskytovatele není možné, doporučujeme předgenerovat datové soubory ve vhodném
datovém formátu a poskytnout soubor ve formátu Atom s odkazy na takto vytvořené
soubory, podobně jako se k tomu kloní implementační pravidla INSPIRE.

Pro datové sady, které se *mění v čase* a jsou příliš velké na to, aby se s každou
změnou vydávala aktualizovaná verze celé sady, je vhodné publikovat jednou v
pravidelných intervalech stavová data a současně k nim poskytovat v kratších
časových intervalech změnové soubory. Toto řešení může výrazně snížit zatížení
IT infrastruktury, neboť uživatele nemusí vždy stahovat celou datovou sadu ve
formě stavových dat, ale pouze menší změnové soubory, které si sami aplikují na
kopii datové sady tak, aby ji měli co možná nejaktuálnější. Více k tomuto tématu
v kapitole Předgenerované soubory a formát Atom. Více o časových řadách v části
:ref:`casove_rady`.

.. _casove_rady:

Verzování dat a časové řady
---------------------------

Geografická data nejsou již delší dobu omezena pouze na dvoudimenzionální
prostor (2D). Data jsou často třídimenzionální (3D a to jak gridová - volumes,
tak vektorová). Mohou být ale i n-dimenzionální (v případě pásem družicových
snímků). V případě časoprostorových dat je dalším rozměrem, který je potřeba
zohlednit, čas. Potom mluvíme o 4D datech.

Časové řady prohlížecích služeb
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Standard OGC WMS nabízí možnost, jak definovat další dimenze pro poskytovaná
data. Nejčastější formou použití je právě čas, ale může to být např. nadmořská
výška, teplota, atd. či případně i jejich kombinace. V metadatech služby lze
uvést buď přesnou časovou specifikaci výčtem časových okamžiků nebo počáteční
čas a velikost časového kroku mezi jednotlivými datovými vrstvami. Příklady jsou
uvedeny v příloze B.

Standard OGC WMTS navíc umožňuje definovat různé dimenze k předgenerovaným
datovým sadám. Princip je podobný jako u zmíněného standardu OGC WMS, příklady
jsou uvedeny v příloze C.

Časové řady stahovacích služeb
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**OGC Web Feature Service**

Standard OGC Web Feature Service (WFS) nemá přímou podporu pro časovou dimenzi.
Standard odkazuje na OGC Filter Encoding Specification (FES) [ref49]_, pomocí
kterého lze filtrovat požadovaná data na základně požadavků ze strany klienta.
Pomocí FES lze nastavit počáteční a koncový hraniční čas (startTime a endTime),
mezi kterými klient požaduje stáhnout data. Verzovat lze také pomocí vlastních
klíčových slov (např. “1.2.3” a podobně).

Z uvedeného vyplývá, že WFS slouží jako rozhraní k datové sadě, která obsahuje
data v různých časových intervalech. Na data vztažená k určitému časovému
okamžiku se lze dotazovat právě pomocí filtru dle standardu OGC FES 2.0.

**OGC Web Coverage Service**

OGC WCS podporuje ve své nejnovější verzi specifikace [ref50]_ časový rozsah
požadovaných dat jako jeden z možných rozměrů. Syntaxe pro definici času sleduje
stejně jako u výše zmíněných služeb technickou normu ISO 8601. Příklad je uveden
v příloze D.

Podle ústního sdělení editora standardu OGC WCS Petra Baumana, se momentálně v
rámci organizace OGC téma času zásadním způsobem mění, neboť se začínají
zohledňovat různé kalendáře (historické, i používané v různých kulturách či
technických společnostech) a další s touto problematikou související komplikace.
Viditelné je to zejména na tom, že ve starších verzích standardů býval definován
parametr TIME explicitně jako vstupní parametr. U nových verzích standardů se
čas mění v jeden z rozměrů dat. Stejně jako stávající rozměry mají své zobrazení
a souřadnicový systém, musí mít i čas společnou referenci.

Verzování a časové řady u souborových formátů a jejich distribuce
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**OGC GeoPackage**

Formát OGC GeoPackage [ref39]_ je postavený na souborové databázi SQLite (viz
kapitola OGC GeoPackage), což umožňuje v porovnání se stávajícími souborovými
formáty pokročilejší funkce pro dotazování a manipulaci s daty pomocí jazyka
SQL. Lze využít standardních datových typů TIME a DATETIME jako atributu daného
geoprvku. Další důležitou vlastností je metadatová tabulka gpkg_content,
obsahující mimo jiné informace last_change (datový typ DATETIME) pro jednotlivé
tabulky (datové vrstvy). Dále existuje metadatová tabulka gpkg_metadata,
obsahující vlastnost timestamp, kterou lze využít na označení aktuálnosti
libovolné jednotky v souboru - buď celé databáze, jednotlivé tabulky či
geoprvku, tj. záznamu v tabulce.

**Verzování systémem Git**

Git je systém na správu verzí, nejčastěji textových souborů, viz kapitola
GitHub. To znamená, že pomocí Gitu lze udržovat přehled o souborech, o tom, kdo
je měnil a jaké změny provedl. Případné konfliktní změny lze řešit poměrně
komfortně, lze se “vracet v čase”, získat stav souboru k určité revizi nebo
časovému okamžiku. Soubor s daty by měl být v Gitu uložen ideálně v textové
podobě (GML, GeoJSON, …). Binární formáty lze technicky vzato spravovat v
prostředí Git také, potom ale nelze využít specializované verzovací nástroje.

**Poskytování datových souborů (RÚIAN best practice)**

ČÚZK zavedl pro distribuci dat Registru Územní Identifikace, Adres a Nemovitostí
(RÚIAN) systém měsíční aktualizace stavových dat s denními dávkami změnových
vět. Tento systém plně pokryje jak potřeby uživatele, který potřebuje
jednorázově získat podkladová data, tak uživatele, který potřebuje udržovat
aktuální obraz celé databáze, aniž by byl nucen stahovat velké objemy dat po
síti. Možnost získat seznam přírůstků od libovolného data zvyšuje na straně
uživatele pružnost procesu aktualizace dat. Datové sady jsou nabízeny v různě
obsáhlých verzích, v některých případech je dokonce možné volit generalizované
hranice. Data jsou nabízena buď pro celé území České republiky, anebo po
jednolivých obcích. To umožňuje při poměrně malé zátěži na straně serveru
efektivně obsloužit velké množství klientů. Práce s aktualizací dat se přesouvá
ze strany serveru ke klientům.

V jedné věci se však RÚIAN nechová ideálně: Jednotlivé soubory a změnové věty
mají sice pevnou a strojově předvídatelnou strukturu, chybí jim však centrální
strojově zpracovatelný zdroj. Tím by mohl být například zmiňovaný formát Atom
(viz :ref:`atom`). Podle ústního sdělení bude Atom v nejbližší době doplněn [#cuzk-atom]_.

.. index::
    single: Metadata
    single: ISO 19115
    single: ISO 19139
    pair OGC CSW, CSW

Metadata
--------
Veškerá publikovaná geodata a na ně navazující webové služby je potřeba opatřit
příslušnými metadaty.  Metadata jsou strukturovaná data o datech. Metadata
popisují data a služby ve strojově zpracovatelném formátu tak, aby bylo možné v
jich automaticky vyhledávat a to i na základě jejich relevance a aktuálnosti.
Pro metadata existuje množstí standardů a doporučení, ale zdaleka ne všechny
jsou vhodné pro oblast geodat.

Vlastní metadata mohou (měly by) mít jak vlastní datové sady (kdo je vytvořil,
kdy, s jakou přesností, co přibližně obsahují, z jaké oblasti přibližně data
jsou atd.), tak i webové služby tyto datové sady publikující (kdo provozuje
danou službu, jaké datasety služba publikuje, atd.).

V současné době je pro pořizování a uchovávání metadat v
geodatové doméně klíčová  mezinárodní technická norma ISO 19115 [ref32]_. Tuto normu
navíc vyžaduje i evropská směrnice INSPIRE ve svém nařízení komise o metadatech
[ref33]_. Vlastní technickou implementací této normy se zabývají implementační
pravidla směrnice INSPIRE pro metadata [ref34]_. Vlastní fyzické uložení metadat
geografické datové sady nebo služby je definováno navazující technickou normou
ISO 19139 (XML) [ref35]_. Obecně lze říci, že je vhodné držet se metadatového
profilu České republiky [ref36]_, i když to v první fázi za vysloveně nutné
nepovažujeme. Důležité je, aby metadata byla dostupná přes rozhraní webové
služby OGC Catalog Service for Web (CSW) [ref37]_. Zároveň doporučujeme tuto službu
otestovat na dostupném software (Esri ArcGIS, QGIS a další) tak, aby byla
ověřena její praktická funkčnost a dostupnost na různých platformách.

Pro úplnost je potřeba dodat, že postupně do domény geografických informačních
systémů a geodat pronikají vznikající standardy pro obecná otevřená data a to se
týká i metadat. Otevřená provázaná data (open linked data) mají vlastní
metadatové standardy, které jsou již v souladu s INSPIRE mapovatelné tak, aby
bylo v těchto datových souborech možné vyhledávat pomocí OGC CSW a obráceně,
linkovaná geodata je možné publikovat na portálech s otevřenými daty.

.. rubric:: Poznámky pod čarou

.. [#shp] Shoda napříč programy panuje alespoň na souboru s příponou .prj, který
    obsahuje informace o souřadnicovém systému.

.. [#agregace] *Agregace* je seskupení vybrané části určitých entit za účelem
    vytvoření nové entity -- seskupení datových prvků do větších skupin.  Tím
    dochází k odstranění některých detailů z dat. Agregace se může použít např.
    pro znepřesnění nebo anonymizaci citlivých dat.

.. [#cuzk-atom] Ústní sdělení, konference "Inspirujme se ...", 2014

.. [#geopackage] Formát OGC GeoPackage byl navržen primárně jako
                 výměnný formát. Nejedná se o alternativu ke geodatabázím
                 jako je např. SpatiaLite, které nabízejí podporu pro
                 pokročilé prostorové SQL dotazy *(spatial SQL queries)*.
