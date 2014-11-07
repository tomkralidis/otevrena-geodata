Příloha A: Vhodný Open Source software pro jednotlivé úlohy
===========================================================

Geodatabáze PostGIS
-------------------

PostGIS [60]_ je nadstavba open source objektově-relační databáze PostgreSQL
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

Mapový server MapServer
-----------------------

Program MapServer [66]_ je tradiční Open Source software pro distribuci geodat.
Podporuje relevantní standardy OGC, díky napojení na knihovnu GDAL umožňuje
export do požadovaných formátů v rámci webových služeb, podporuje časovou složku
u služby OGC WMS. Díky nadstavbě MapCache umožňuje generovat dlaždice a
nabídnout je prostřednictvím OGC WMTS. Při porovnání jednotlivých dostupných
implementací OGC WMS se ukázalo, že se jedná o nejrychlejší software ze všech
zúčastněných [67]_.

Knihovna GDAL
-------------

Knihovna GDAL [59]_ je bezesporu základním kamenem Open Source GIS ekosystému.
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

PyCWS
-----

PyCWS [69]_ je serverová implementace standardu OGC CWS napsaná v jazyce Python.
PyCWS umožňuje publikovat a vyhledávat v metadatech geografických datových sad.
Pomocí tohoto serverového řešení lze postavit v rámci infrastruktury geodat
(SDI) katalog metadat odpovídající v současnosti platné technické normě ISO,
evropské směrnici INSPIRE  a souvisejícím národním profilům. PyCWS je
certifikovaný OGC software.
