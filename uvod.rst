.. index:: 
    single: Veřejná správa
    single: CKAN
    single: Open Data Handbook
    single: OpenStreetMap
    single: 
Úvod
====
Je všeobecně uznávaným faktem, že sebelepší řešení není udržitelné, pokud není
naplněno kvalitními a aktuálními daty. V poslední době dochází v této
souvislosti v čím dál větší míře ke sdílení a šíření dat prostřednictvím sítě
Internet. Pojmy jako *“linked data”* nebo *“sémantický web”* nejsou dávno jen
teoretickým konceptem, ale aktuální skutečností. Bez nadsázky lze říci, že data
jsou jedna z komodit, které podporují jak technický pokrok, tak rozvoj občanské
společnosti. Tento fakt začíná být po vzoru našich nejbližších sousedů,
především Německa, ale i Rakouska či Velké Británie reflektován i veřejnou
správou v České republice v podobě postupného otevírání dat. 

Právě ve Velké Británii vznikly dva celosvětově nejvýznamnější hnutí v
otevírání dat. Prvním z nich je nezisková organizace `Open Knowledge
Foundation <http://cz.okfn.org/>`_ (OKFN), která se orientuje na
propagaci otevřenosti ve znalostech a datech obecně. OKFN stojí mimo
jiné za projektem katalogu CKAN [ref45]_ a tzv. `Open Data Index
<http://global.census.okfn.org/>`_ (žebříček otevřenosti dat). Tento
žebříček shrnuje úroveň států z pohledu otevřenosti a dostupnosti
nejdůležitějších datových sad jako jsou např. jízdní řády, státní
rozpočet, výsledky voleb, obchodní rejstřík a podobně. Základní
zkušenosti s právními, sociálními a technickými aspekty OKFN shrnuje
publikace *Open Data Handbook* [ref70]_, ze které částečně čerpá i tato
analýza. Druhým z uvedených hybatelů je projekt `OpenStreetMap
<http://www.openstreetmap.org/about>`_ (OSM), který byl založen v
roce 2006 právě ve Velké Británii s cílem komunitního vytváření volně
dostupných geografických dat a následně jejich vizualizace do podoby
silniční mapy, uličního plánu měst a dalších výstupů. Vzhledem k tomu,
že je od počátku založen na kolektivní spolupráci a na koncepci Open
Source, se rychle rozšířil do celého světa. Data z projektu OSM jsou
poskytována pod otevřenou licencí `Open Database Licence
<http://opendatacommons.org/licenses/odbl/>`_.

Veřejná správa vždy shromažďovala data potřebná pro výkon svých agend.
Zpřístupnění těchto dat umožní veřejnosti nejen využít informace v nich
obsažené, ale především řádově znásobit jejich hodnotu tím, že kdokoliv nad nimi
bude moci bez jakéhokoliv omezení postavit vlastní aplikaci či službu, anebo je
podrobit nezávislé analýze. Právě proto je důležité, aby co nejvíce dat
vytvářených veřejnou správou bylo publikováno a volně poskytováno široké
veřejnosti k dalšímu užití. Jen tak může být zcela beze zbytku využit potenciál
dat sbíraných z veřejných prostředků.

Otevírání dat je proces, který se týká několika oblastí. Kromě technických
záležitostí se jedná především o licenční politiku, která v ideálním případě
umožní vývojářům navazujících aplikací data předávat dál a vytvářet nad nimi
další odvozená díla, která nebudou zatěžována žádnými restrikcemi či omezeními.

Obsahem této analýzy jsou zejména geografická data (tzv. *geodata*),
která se ve velké míře řídí na rozdíl od ostatních typů dat vlastními
zvyklostmi, standardy či technickými normami. Proces standardizace je
v oblasti geoinformačních technologií, na rozdíl od jiných
technologických oblastí, podporován již delší dobu, což výrazně
ulehčuje tvorbu dalších doporučení. V současnosti drtivá většina
výrobců softwarových produktů (proprietárních i otevřených), ale
např. i Evropská komise skrze směrnici `INSPIRE
<http://inspire.gov.cz/>`_ navazuje na existující standardy v oblasti, které
pomáhá dále rozvíjet. Ty jsou vytvářeny mezinárodní standardizační
organizací `Open Geospatial Consortium
<http://www.opengeospatial.org/>`_ (OGC) a technickou komisí `ISO TC
211 <http://www.isotc211.org/>`_.  Mezinárodní technické normy ISO mohou následně být přejímány jako normy
národní (označné jako ČSN EN ISO, například ČSN EN ISO 19136 *Geografická informace
– Značkovací jazyk geografie (GML)* [ref77]_). 

.. index::
    pair: Otevřená data; Open Data
    pair: Pěti hvězdičkový systém; Fivestar system

Otevřená data
-------------

Aby data mohla být označena za *otevřená*, musí splňovat několik
legislativních a technických podmínek (viz níže). Tyto podmínky nejsou v čase
konstantní, vyvíjí se spolu s technickými prostředky, standardy ale i
legislativou či postoji společnosti.

V současnosti těmito podmínkami myslíme zejména:

* Data jsou dostupná na síti Internet a dohledatelná běžnými nástroji.
* Data jsou čitelná, tedy v textovém či binárním formátu.
* Data musí být úplná, tj. jsou zveřejněná v takovém rozsahu, aby nechyběly
  některé fragmenty umožňující jejich využití. Data by zároveň měla být
  zveřejněna v maximálním možném rozsahu.
* Legislativní a technické překážky pro využití dat jsou minimální.

.. _pet-hvezdicek:
  
Otevírání dat přináší kromě nákladů na vlastní otevření a provoz také nemalé
přínosy jak pro poskytovatele, tak pro uživatele. Tim Berners-Lee [ref15]_ sestavil
tzv. *pětihvězdičkový systém* hodnocení otevřenosti dat, jehož smyslem je umožnit
jednoduchou orientaci ve stupni otevřenosti datových sad. Čím výše se datová
sada dostane, tím větší je možnost jejího využití veřejností.

.. figure:: imgs/opendata.png
   :scale: 100 %
   :alt: Pěti hvězdičkový systém otevřených dat
   :align: center
   
   *Pěti hvězdičkový systém otevřených dat podle Tim Berners-Lee* [ref15]_

**★ Dostupná data**

    Data jsou zveřejněna na Internetu, nezáleží na formátu.
    Data, která jsou zveřejněna na síti Internet v jakémkoli  formátu, ale pod
    otevřenou licencí pro jejich využití. Existují tedy určitá technická omezení pro
    jejich využití, nicméně legislativní omezení jsou odstraněna. Příkladem může být
    mapové dílo ve formátu `PDF <http://cs.wikipedia.org/wiki/Portable_Document_Format>`_.

**★★ Strukturovaná data**

    Data jsou zveřejněna ve strojově čitelném formátu.  Data jsou
    zveřejněna ve strojově zpracovatelném formátu, který není
    otevřený.  Příkladem mohou být data ve formátu `Microsoft Excel
    <http://cs.wikipedia.org/wiki/Microsoft_Excel>`_ nebo data uložená
    v `Esri GeoDatabase
    <http://cs.wikipedia.org/wiki/Geodatab%C3%A1ze#Souborov.C3.A1_geodatab.C3.A1ze_.28File_geodatabase.29>`_.

**★★★ Data v otevřeném formátu**

    Data jsou zveřejněna v otevřeném formátu.  Strojový formát, ve
    kterém jsou data zveřejněna, je otevřený, tj. veřejně publikovaný
    s licencí umožňující jeho využití. Příkladem jsou například
    formáty `Geospatial Markup Language
    <http://www.opengeospatial.org/standards/gml>`_ (GML), `OGC
    GeoPackage <http://www.opengeospatial.org/standards/geopackage>`_
    nebo `Esri Shapefile <http://cs.wikipedia.org/wiki/Shapefile>`_.

**★★★★ Data s identifikátorem**

    Data jsou dohledatelná, mají unikátní identifikátor. Data jsou
    opatřena identifikátorem `Uniform Resource Identifier
    <http://cs.wikipedia.org/wiki/Uniform_Resource_Identifier>`_
    (URI), unikátním v rámci celé sítě Internet. Jednotlivé prvky
    datové sady by měly být identifikované pomocí URI ve tvaru
    použitelném pro protokol `HTTP
    <http://cs.wikipedia.org/wiki/Hypertext_Transfer_Protocol>`_,
    tzn. v podobě adresy URL. Tím se zajistí, že uživatelé mohou daný
    prvek kdykoli najít.

**★★★★★ Provázaná data**

    Data jsou navzájem prolinkovaná, lze mezi nimi
    navigovat, “surfovat” [ref71]_.  Data jsou nejen identifikovatelná pomocí URI, ale
    obsahují odkazy na další datové sady.  Stejně jako datové sady jsou pomocí
    odkazů provázány i jednotlivé prvky z datových sad. Data jsou dále opatřena
    popisnými informacemi (metadaty) tak, aby v nich bylo možno jednoduše
    vyhledávat. 

Výhody ☑ a omezení ☒ – z hlediska uživatele
-------------------------------------------

.. tabularcolumns:: |p{.1\textwidth}|p{.8\textwidth}|
+-------+---------------------------------------------------------------------------------+
| ★     | ☑ Data lze prohlížet                                                            |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data lze tisknout                                                             |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data lze uložit na lokální disk                                               |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data lze vložit do dalšího systému nebo databáze                              |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data lze podle potřeby a možností použitého formátu měnit, doplňovat          |
|       | či odvozovat další produkty                                                     |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data je možné sdílet s dalšími uživateli                                      |
+-------+---------------------------------------------------------------------------------+
| ★★    | ☑ Data lze automaticky zpracovávat pomocí proprietárního software               |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Data lze vyexportovat do jiného formátu                                       |
+-------+---------------------------------------------------------------------------------+
| ★★★   | ☑ Uživatel může manipulovat s daty, aniž by byl závislý na vlastnictví          |
|       | konkrétního, většinou proprietárního software                                   |
+-------+---------------------------------------------------------------------------------+
| ★★★★  | ☑ Uživatel může na data odkazovat z kteréhokoli jiného místa na webu            |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Lze pořizovat trvalé odkazy na data                                           |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Lze znovu použít část dat, aniž by se musela vytvářet jejich fyzická kopie    |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Lze kombinovat datové sady mezi sebou, protože použité URI jsou vždy unikátní |
+-------+---------------------------------------------------------------------------------+
|       | ☒ Porozumění struktuře takto publikovaných otevřených dat je                    |
|       | komplikovanější, než pochopení jednoduché tabelární nebo stromové struktury     |
+-------+---------------------------------------------------------------------------------+
| ★★★★★ | ☑ Lze najít další datové sady při procházení té současné                        |
+-------+---------------------------------------------------------------------------------+
|       | ☑ Datové sady jsou publikovány v jasně definovaném schématu                     |
+-------+---------------------------------------------------------------------------------+
|       | ☒ Možnost výskytu neexistujících cílů, které je potřeba ošetřit,                |
|       | podobně jako když na webovém serveru neexistuje požadovaná adresa               |
+-------+---------------------------------------------------------------------------------+
|       | ☒ Prezentace dat z externích zdrojů jako ověřený fakt je riskantní              |
+-------+---------------------------------------------------------------------------------+

Výhody ☑ a omezení ☒ – z hlediska poskytovatele
-----------------------------------------------

.. tabularcolumns:: |p{.1\textwidth}|p{.8\textwidth}|
+--------+---------------------------------------------------------------------------------------+
| ★      | ☑ Odpadá opakovaná činnost související s distribucí dat, uživatelé si je              |
|        | mohou stáhnout z Internetu                                                            |
+--------+---------------------------------------------------------------------------------------+
|        | ☑ Vlastní otevření je většinou snadné a s minimálními náklady                         |
+--------+---------------------------------------------------------------------------------------+
| ★★     | ☑ Otevření dat i uživatelům, kteří mají zájem kromě jejich prohlížení                 |
|        | také o jejich zpracování. Tím se výrazně zvětšuje velikost skupiny uživatelů,         |
|        | kteří budou takto publikovaná data využívat                                           |
+--------+---------------------------------------------------------------------------------------+
|        | ☑ Vlastní otevření je většinou snadné a s minimálními náklady                         |
+--------+---------------------------------------------------------------------------------------+
| ★★★    | ☑ Další rozšíření skupiny potenciálních uživatelů o ty, kteří                         |
|        | nepoužívají programové vybavení kompatibilní s vybavením poskytovatele                |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Náklady na  konverzi a uložení dat do zvolených formátů. Tyto náklady nemusí být v  |
|        | konečném důsledku příliš vysoké, protože konverze mezi jednotlivými formáty je poměrně|
|        | běžná a dobře zvládnutá. Je však třeba s nimi počítat.                                |
+--------+---------------------------------------------------------------------------------------+
| ★★★★   | ☑ Uživatel má velice dobrou kontrolu členění dat a může optimalizovat přístup k nim   |
+--------+---------------------------------------------------------------------------------------+
|        | ☑ Jiní poskytovatelé se mohou na data navázat a tím je zlepšit na úroveň  ★★★★★       |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Většinou je nutný zásah do struktury dat                                            |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Poskytovatel musí přiřadit URI k datům a zabezpečit jejich prezentaci               |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Poskytovatel musí najít existující postupy nebo vytvořit své vlastní                |
+--------+---------------------------------------------------------------------------------------+
| ★★★★★  | ☑ Data jsou dohledatelná a prohledatelná, čímž se výrazně zvyšuje jejich hodnota      |
+--------+---------------------------------------------------------------------------------------+
|        | ☑ Poskytovatel může profitovat ze vzájemného provázání dat, podobně jako uživatelé    |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Poskytoval musí investovat do propojení vlastních dat s dalšími datovými sadami     |
+--------+---------------------------------------------------------------------------------------+
|        | ☒ Poskytoval musí udržovat tato propojení aktuální, pokud možno                       |
|        | odstraňovat propojení vedoucí na již neexistující cíle (např. pokud je nějaká         |
|        | webová stránka odstraněna.                                                            |
+--------+---------------------------------------------------------------------------------------+


