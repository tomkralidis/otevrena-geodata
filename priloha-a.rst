.. index:: 
    single: Open source software

Příloha A: Open Source software pro jednotlivé úlohy
====================================================
Pro jednotlivé úlohy spojené s publikováním otevřených prostorových dat (převod
na správný formát, publikace pomocí služeb nebo statických souborů, validace,
...), je potřeba software. Vždy doporučujeme využít maximálně stávající
technické (software i hardware) vybavení v organizaci dostupné, může se ale
stát, že se ukáže, že stávající platforma je z nějakého důvodu (kapacitní,
licenční, zastaralost, ...) nevhodná.

Zde představené programy jsou mezi uživateli rozšířené a představují obvyklé
řešení při budování geografického informačního systému postaveného na open
source software.  Vývojáři open source software se primárně snaží o maximální
implementaci stávajících standardů (často se jedná o referenční implementace) a
maximální operabilitu. Také proto jsou tyto systémy vhodné i v hybridních systémech
kombinujících software s otevřeným i uzavřeným zdrojovým kódem. 

Je iluzorní automaticky předpokládat, že použitím open source software musí
nutně dojít k významnému ušetření finančních prostředků v dané organizaci.
Především záleží na kvalitě pracovníků, kteří se mohou, ale nemusejí spolehnout
na vlastní síly při údržbě celého systému a od toho se následně odvíjí i cena
celého řešení. V konečné sumě ale odpadají nutné náklady na pořízení software a na
udržování licencí. Open source lze nasadit okamžitě podle potřeb, lze s ním
okamžitě experimentovat a vybudovat potřebné řešení, bez nutnosti vypořádávat
předem licenční otázky.

Seznam zdaleka není kompletní a pro další alternativy doporučujeme navštívit
stránku http://osgeo.org (Open Source Geospatial Foundation), která většinu
programů s otevřeným zdrojovým kódem zaštiťuje.

.. index::
    single: PostGIS

Geodatabáze PostGIS
-------------------

PostGIS [ref60]_ je nadstavba open source objektově-relační databáze PostgreSQL
určená pro práci s geografickými daty. PostGIS lze ve světě Open Source bez
nadsázky považovat za vedoucího hráče na poli geodatabází a jako přímou
alternativu k proprietárnímu Oracle Spatial. Z hlediska správy geodat PostGIS
nabízí mnohem více než jen úložiště dat, ale také mocné dotazovací prostředí,
včetně podpory pro prostorové funkce, integraci topologické správy vektorových
dat a společnou správu pro rastrová data. V posledních verzích PostgreSQL se
objevuje podpora pro formáty jako JSON a jeho binární obdobu BSON, což umožňuje
vybudovat NOSQL databázi a velice efektivně “kešovat” strukturovaná data pro
jejich rychlý a efektivní výdej. To může v případě prozíravě navrženého řešení,
při současném zachování vnitřní integrity dat, podstatně snížit požadavky na IT
infrastrukturu.

Další zjevnou výhodou nasazení PostGIS je jeho provázanost s celým ekosystémem
Open Source, ale i proprietárního softwaru. Pokud tedy budujeme systém, který má
být “bezešvý”, je využití PostGIS idealním řešením.

.. index::
    single: MapServer

Mapový server MapServer
-----------------------

Program MapServer [ref66]_ je tradiční Open Source software pro distribuci geodat.
Podporuje relevantní standardy OGC, díky napojení na knihovnu GDAL umožňuje
export do požadovaných formátů v rámci webových služeb, podporuje časovou složku
u služby OGC WMS. Díky nadstavbě MapCache umožňuje generovat dlaždice a
nabídnout je prostřednictvím OGC WMTS. Při porovnání jednotlivých dostupných
implementací OGC WMS se ukázalo, že se jedná o nejrychlejší software ze všech
zúčastněných [ref67]_.

.. index::
    single: GeoServer

Mapový server GeoServer
-----------------------

Program GeoServer (http://geoserver.org) je tradiční Open Source software pro
distribuci geodat.  Primárně se zaměřuje na implementaci standardů OGC, obsahuje
nadstavby na tvorby rastrových cachí, processingové služby a další. 

GeoServer ja naprogramovaný v jazyce Java a množství práce v něm obstarává
knihovna GeoTools. Na rozdíl od MapServeru disponuje webovým uživatelským
rozhraním, které je pro většinu uživatelů relativně rychle pochopitelné.

.. index::
    single: GDAL
    single: OGR

Knihovna GDAL
-------------

Knihovna GDAL [ref59]_ je bezesporu základním kamenem Open Source GIS ekosystému.
Podporuje čtení a zápis více než 100 nejrůznějších rastrových a více než 80
vektorových formátů včetně proprietárních formátů jako Esri File Geodatabase či
specifických českých formátů VFK a VFR. Díky integrované knihovně Proj.4
podporuje transformaci dat i do těch nejexotičtějších souřadnicových systémů.
Výhodná je kombinace této knihovny s programovacím jazykem Python, která nabízí
uživateli velmi mocný a flexibilní nástroj pro práci  s geodaty. Právě skripty v
jazyce Python by mohly potencionálně tvořit jádro řešení pro otevírání geodat
implementované v Open Source frameworku. Kromě generování souborů či integraci s
mapovým serverem MapServer je možné knihovnu GDAL použít i pro implementaci sady
testů validity a konzistence publikovaných geodat.

.. index::
    single: PyCSW

PyCWS
-----

PyCWS [ref69]_ je serverová implementace standardu OGC CWS napsaná v jazyce Python.
PyCWS umožňuje publikovat a vyhledávat v metadatech geografických datových sad.
Pomocí tohoto serverového řešení lze postavit v rámci infrastruktury geodat
(SDI) katalog metadat odpovídající v současnosti platné technické normě ISO,
evropské směrnici INSPIRE  a souvisejícím národním profilům. PyCWS je
certifikovaný OGC software.

.. index::
    single: GeoNetwork

GeoNetwork
-----------

GeoNetwork (http://geonetwork-opensource.org) je serverová implementace
standardu OGC CWS napsaná v jazyce Java.  GeoNetwork umožňuje publikovat a
vyhledávat v metadatech geografických datových sad.  Pomocí tohoto serverového
řešení lze postavit v rámci infrastruktury geodat (SDI) katalog metadat
odpovídající v současnosti platné technické normě ISO, evropské směrnici INSPIRE
a souvisejícím národním profilům. GeoNewtork je velice oblíbení právě v
organizacích implementujících směrnici INSPIRE.
