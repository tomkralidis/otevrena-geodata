.. index::
    single: Souřadnicové systémy
    single: S-JTSK
    single: UTM
    single: WGS84
    single: S-42
    single: EPSG

Souřadnicové systémy
====================

Systém souřadnic je soustava základních údajů (referenčních bodů, přímek nebo
křivek), umožňující určovat souřadnice polohy objektu ve zvolené vztažné
soustavě. Protože převod tvaru Země na plochu papíru (dnes monitoru počítače) je
vždy provázen určitou nepřesností, existuje množství sytémů, které v daném místě
na Zemi poskytují známé a popsatelné zkreslení-nepřesnost (samozřejmě existují i
globální systémy, používané pro zobrazení celé planety).

.. note:: Protože existuje množství způsobů, jak popsat konkrétní systém a
    celkově velké množství souř. systémů, bývá v oboru zvykem, že se používá databáze 
    EPSG (European Petroleum Survey Group). 
    Tu lze stáhnout ze stránek http://www.epsg-registry.org/ nebo využívat
    některou ze služeb nad touto databází postavenou, např. http://epsg.io

Geografické datové sady jsou v České republice vedeny především v souřadnicovém
systému S-JTSK (EPSG 5514 [#5514]_). Pro vojenské mapové podklady se v minulosti používal
souřadnicový systém S-42 (EPSG 3835 [#3835]_). Vzhledem k zániku Varšavské smlouvy a
pozdějšímu přistoupení k NATO se začal místo souřadnicového systému S-42
používat systém UTM/WGS-84 (zóny 33 - EPSG 32633 [#32633]_ a 34 - EPSG 32634 [#32634]_). Evropská
směrnice INSPIRE [ref26]_ zejména pak ve specifikaci věnované souřadnicovým systémům
([ref29]_, str. VII) dále pro měřítka větší než 1:500 000 mezi podporované systémy
přidává ETRS89-TM (EPSG 3035[#3035]_). Praxe si vynutila použití souřadnicového systému
Spherical Mercator (EPSG 3857[#3857]_), zavedeného firmou Google pro jejich mapové
produkty.

.. note:: Dříve používané zápisy S-JTSK, jako EPSG:2065[#2065]_, ESRI/ESPG:102067[#102067]_
    vznikly díky tomu, že v databázi EPSG nebyl přítomný kód pro Křovákovo zobrazení
    s "otočenými osami" (a zápornými hodnotami souřadnic), tzv. "S-JTSK/Krovak
    East North". To dnes již není potřeba a všechny systémy by měly nadále
    používat EPSG:5514

Obecná doporučení pro souřadnicové systémy
------------------------------------------

Pro stahovací služby se přikláníme k publikování datových sad v jejich původních
souřadnicových systémech, což je v praxi většinou S-JTSK. Navíc všechny
relevantní desktopové GIS programy jsou schopny transformovat geodata do
uživatelem požadovaných cílových souřadnicových systémů za běhu. Pokud se přeci
jen ukáže, že je potřeba poskytnout některým klientům možnost stahovat data v
jiném souřadnicovém systému, doporučujeme zprovoznit transformační souřadnicovou
službu podle specifikace INSPIRE [ref30]_.

V každém případě je potřebné zajistit, aby distribuovaná data měla korektně
nastaveny definice souřadnicových systémů. V případě S-JTSK je nutné, aby
informace o souřadnicovém systému obsahovala parametry pro transformaci mezi
referenčním Besselovým elipsoidem a elipsoidem WGS-84 nebo tzv. transformační
parametry anebo grid, jinak může dojít k nepřesnosti při transformaci až v řádu
několika desítek metrů. Více informací k tomuto tématu lze najít například na
Portálu FreeGIS [ref31]_.

Vedle S-JTSK doporučujeme nabízet data v souřadnicovém systému WGS84 (EPSG
4326[#4326]_). Zejména zahraniční uživatelé či uživatelé kombinující data z různých
datových zdrojů tento souřadnicový systém využijí. Kromě toho se používá v
navigacích a GPS zařízeních.

U prohlížecích služeb je vhodné umožnit zobrazení dat v souřadnicovém systému
Spherical Mercator, využívaný např. firmou Google ve svých mapových produktech,
projektem OpenStreetMap a nebo mapami Bing. To uživatelům umožní využívat tyto
zobrazovací služby v kombinaci s jinými podklady. Tento systém nesl kdysi
neoficiální označení 900913, nyní je již zastaralý a v EPSG je označen kódem
3857.

Obecně lze říci, že na běžných platformách webových serverů je přidání dalšího
souřadnicového systému otázku minimálního zásahu do konfigurace, takže lze
podporu pro další systémy přidávat i na požádání.

Pořadí souřadnic v WMS 1.3.0, WFS 2.0.0 a GML 3.x
-------------------------------------------------

Ve starších verzích standardů OGC se předpokládalo, že pořadí souřadnic v
požadavku (např. parametru BBOX u WMS) nebo při odpovědi (např. GML publikované
serverem WFS) je vždy ve formátu X,Y.

V nových verzích standardů (WMS 1.3.0, WFS 2.0.0, atd.) je explicitně
zdůrazněno, že záleží na předpisu daného souřadnicového systému - pořadí os tedy
může být X,Y ale i Y,X. To platí zejména pro souřadnicové systémy WGS-84 (EPSG
4326) a ETRS-89 (EPSG 3035). U S-JTSK (EPSG 5514) se tento fakt v praxi
nezohledňuje.

Zdaleka ne všechny serverové ale i klientské implementace standardů jsou schopny
pořadí souřadnic korektně zohlednit [ref54]_, což je dobré mít na paměti.

Doporučení pro prohlížecí a stahovací služby
--------------------------------------------

OGC WMTS
~~~~~~~~

Pro prohlížecí službu OGC WMTS je výhodné nabízet předgenerované dlaždice
minimálně pro souřadnicové systémy EPSG 3857 (Spherical Mercator) a to ve
schématu, ve kterém je nabízí např. mapy firmy Google, ale i projekt
OpenStreetMap [ref52]_ (ale nakonec i služby ČÚZK) a pro souřadnicový systém S-JTSK
(EPSG 5514) ve schématu používaném servery ČÚZK [ref53]_.

OGC WMS,  WFS a WCS
~~~~~~~~~~~~~~~~~~~

Transformace mezi souřadnicovými systémy bývá u současných software poměrně
rychlá. Opět platí, že služby by měly nabízet data především v původním
souřadnicovém systému - převážně S-JTSK (EPSG 5514). Vzhledem k určité
exotičnosti tohoto systému je vhodné navíc podporovat minimálně ETRS-89 (EPSG
3035) a WGS84 (EPSG 4326). Spherical Mercator (EPSG 3857) není v tomto případě
nezbytný, většina webových prohlížeček transformuje vektorová data z WGS84
automaticky, stejně tak většina desktopových nástrojů.

Doporučení pro předgenerované vektorové a rastrové soubory
----------------------------------------------------------

Vzhledem k plánovaným větším objemům dat doporučujeme publikovat datové soubory
v původním souřadnicovém systému (S-JTSK, EPSG 5514) a případně WGS84 (EPSG
4326). Implementační pravidla směrnice INSPIRE doporučují poskytnout
transformační službu, která umožní na straně serveru transformovat data přímo do
cílového systému.

.. rubric:: Poznámky pod čarou

.. [#2065] http://epsg.io/2065
.. [#5514] http://epsg.io/5514
.. [#102067] http://epsg.io/102067
.. [#32633] http://epsg.io/32633
.. [#32634] http://epsg.io/32634
.. [#4326] http://epsg.io/4326
.. [#3857] http://epsg.io/3857
.. [#3835] http://epsg.io/3835

