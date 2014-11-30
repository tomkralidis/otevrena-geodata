==============================================
Otevírání geografických dat - Případová studie
==============================================

.. rubric:: Anotace

Tato případová studie shrnuje výsledky konzultací pro otevírání
geografických dat, provedených ve prospěch `Institutu plánování a
rozvoje hlavního města Prahy <http://www.iprpraha.cz/>`_ (*IPR Praha*),
který vznik dokumentu finančně podpořil. Zástupci IPR Praha měli
velice kvalifikovaný a ucelený názor na celou problematiku. Konzultace
byly zaměřeny na celkový koncept otevírání dat a na technické pasáže,
kde byla potřeba většího detailu, doporučení vhodného postupu,
případně navržení řešení.  Tomu odpovídá i struktura dokumentu, která
nemusí být vždy zcela přehledná a dostatečně obecná.

Na základě našich zkušeností z praxe nastiňuje případná technická úskalí a
problémy, se kterými je třeba počítat, mají-li být publikovaná data dostupná co
nejširšímu okruhu uživatelů. Spíše než jednotlivými nástroji, které jsou v mnoha
ohledech věcí osobních preferencí, jsme se zabývali obecnými principy, které je
v souvislosti s otevíráním geodat potřeba respektovat. V textu jsme se snažili
maximálně zúročit naše praktické zkušenosti s různě kvalitními geografickými
daty a informačními systémy pro jejich správu. Cílem bylo shromáždit a utřídit
přehled témat, které usnadní navržení konkrétního řešení pro otevírání geodat.

.. rubric:: Licence

..
            .. image:: imgs/cc-by-sa.png
           
Tento dokument podléhá licenci *Creative Commons 4.0
BY-SA*. Informace o podrobnostech licence najdete na adrese
http://www.creativecommons.cz/.

.. rubric:: Spolupráce

Text studie můžete stáhnout ze serveru `GitHub
<https://github.com/OpenGeoLabs/otevrena-geodata/>`_ a dále rozšiřovat
standardními postupy (*fork*, *pull request*).

.. raw:: latex
    
         \clearpage
.. rubric:: Revize dokumentu

.. tabularcolumns:: |p{2cm}|p{1.5cm}|p{4cm}|p{6.5cm}|
         
+------------+------------+-------------------------------+---------------------------------+
| **Datum**  | **Revize** | **Editoři**                   | **Popis**                       |
+============+============+===============================+=================================+
| 2014-09-30 | 1.0.0      | Jáchym Čepický, Martin Landa, | První verze dokumentu           |
|            |            | Radek Augustýn, Jan Cibulka,  |                                 |
|            |            | Jan Michálek                  |                                 |
+------------+------------+-------------------------------+---------------------------------+
| 2014-10-03 | 1.0.1      | Radek Augustnýn               | Drobné revize formátování       |
+------------+------------+-------------------------------+---------------------------------+
| 2014-10-05 | 1.0.2      | Jáchym Čepický, Martin Landa, | Jazyková korektura textu.       |
|            |            | Radek Augustýn, Jan Michálek  |                                 |
+------------+------------+-------------------------------+---------------------------------+
| 2014-11-03 | 2.0.0      | Jáchym Čepický, Martin Landa, | Druhá verze dokumentu.          |
|            |            | Radek Augustýn, Jan Michálek  | Zapracování připomínek          |
|            |            |                               | IPR Praha.                      |
+------------+------------+-------------------------------+---------------------------------+
| 2014-12-01 | 2.1.0      | Jáchym Čepický, Martin Landa  | Převod dokumentu do             |
|            |            |                               | formátu reStructuredTex a jeho  |
|            |            |                               | publikování na serveru          |
|            |            |                               | Git\-Hub.                       |
+------------+------------+-------------------------------+---------------------------------+
| 2014-12-01 | 2.2.0      | Jáchym Čepický, Martin Landa  | Revize textu dle připomínek     |
|            |            |                               | zástupců IPR Praha, seznam      |
|            |            |                               | zkratek, přeformátování         |
|            |            |                               | struktury.                      |
+------------+------------+-------------------------------+---------------------------------+

.. raw:: latex
    
         \clearpage

.. rubric:: Seznam zkratek

.. todo:: Doplnit zkratky

.. tabularcolumns:: |p{5cm}|p{9cm}|
         
+------------+-----------------------------------------------------------------+
| **Zkratka**| **Význam**                                                      |
+============+=================================================================+
| ATOM       | Atom Syndication Format) je webový standard pro publikování     |
|            | syndikovaného obsahu (obsahu, kterému byly zpětně dodán aktuální|
|            | informace)                                                      |
+------------+-----------------------------------------------------------------+
| CSV        |                                                                 |
+------------+-----------------------------------------------------------------+
| CSW        |                                                                 |
+------------+-----------------------------------------------------------------+
| ČSN        |                                                                 |
+------------+-----------------------------------------------------------------+
| EPSG       | European Petroleum Survey Group. Jedná se o široce využívanou   |
|            | databázi zemských elipsoidů, geodetických dat, zeměpisných a    |
|            | kartografických souřadnicových systémů, měrných jednotek, atd.  |
+------------+-----------------------------------------------------------------+
| GeoTIFF    |                                                                 |
+------------+-----------------------------------------------------------------+
| GeoJSON    |                                                                 |
+------------+-----------------------------------------------------------------+
| GIF        | Graphics Interchange Format, formát souboru určený pro rastrovou|
|            | grafiku                                                         |
+------------+-----------------------------------------------------------------+
| GIS        |                                                                 |
+------------+-----------------------------------------------------------------+
| GML        |                                                                 |
+------------+-----------------------------------------------------------------+
| INSPIRE    |                                                                 |
+------------+-----------------------------------------------------------------+
| ISO        |                                                                 |
+------------+-----------------------------------------------------------------+
| JSON       |                                                                 |
+------------+-----------------------------------------------------------------+
| JPEG       | Metoda ztrátové komprese používané pro ukládání počítačových    |
|            | obrázků ve fotorealistické kvalitě. Též formát souboru          |
|            | obsahující data (obrázek) pomocí této metody komprimovaná.      |
+------------+-----------------------------------------------------------------+
| KML        |                                                                 |
+------------+-----------------------------------------------------------------+
| LPIS       |                                                                 |
+------------+-----------------------------------------------------------------+
| OGC        | Open Geospatial Consortium,  mezinárodní standardizační         |
|            | organizace pro oblast GIS a geoprostorových dat                 |
+------------+-----------------------------------------------------------------+
| OSM        |                                                                 |
+------------+-----------------------------------------------------------------+
| OWS        | Open Web Services, skupina otevřených webových služeb podle     |
|            | standardů OGC                                                   |
+------------+-----------------------------------------------------------------+
| PNG        |                                                                 |
+------------+-----------------------------------------------------------------+
| RUIAN      |                                                                 |
+------------+-----------------------------------------------------------------+
| SHP        | Formát vektorových dat Esri Shapefile                           |
+------------+-----------------------------------------------------------------+
| S-JTSK     |                                                                 |
+------------+-----------------------------------------------------------------+
| SOS        | Sensor Observation Service, standard OGC OWS (otevřené webové   |
|            | služby podle OGC). SOS umožňuje klientům získat ze serverů různá|
|            | sensorová data a údaje o pozorování z nich.                     |
+------------+-----------------------------------------------------------------+
| SQL        |                                                                 |
+------------+-----------------------------------------------------------------+
| TIFF       |                                                                 |
+------------+-----------------------------------------------------------------+
| TMS        |                                                                 |
+------------+-----------------------------------------------------------------+
| TopoJSON   |                                                                 |
+------------+-----------------------------------------------------------------+
| URI        |                                                                 |
+------------+-----------------------------------------------------------------+
| URL        |                                                                 |
+------------+-----------------------------------------------------------------+
| VDP        |                                                                 |
+------------+-----------------------------------------------------------------+
| VFR        |                                                                 |
+------------+-----------------------------------------------------------------+
| WCS        | Web Coveradge Service, standard OGC OWS (otevřené webové služby |
|            | podle  OGC), umožňující klientovi požadovat po serveru obrazová |
|            | (rastrová) data                                                 |
+------------+-----------------------------------------------------------------+
| WFS        | Web Feature Service, standard OGC OWS (otevřené webové služby   |
|            | podle  OGC), umožňující klientovi požadovat po serveru vektorová|
|            | data                                                            |
+------------+-----------------------------------------------------------------+
| WGS        |                                                                 |
+------------+-----------------------------------------------------------------+
| WMS        | Web Map Service, standard OGC OWS (otevřené webové služby podle |
|            | OGC), umožňující klientovi požadovat po serveru vyrenderované   |
|            | obrázky mapových kompozic                                       |
+------------+-----------------------------------------------------------------+
| WMTS       |                                                                 |
+------------+-----------------------------------------------------------------+
| WWW        | World Wide Web, soustava propojených hypertextových (na sebe    |
|            | navzájem odkazujících dokumentů                                 |
+------------+-----------------------------------------------------------------+
| XML        |                                                                 |
+------------+-----------------------------------------------------------------+
| XSD        |                                                                 |
+------------+-----------------------------------------------------------------+
| XSLT       |                                                                 |
+------------+-----------------------------------------------------------------+


.. toctree::
    :maxdepth: 2

    uvod
    pozitiva
    uzivatele
    licence
    opendata
    sour-systemy
    otevirani
    technicke-reseni
    bib

.. raw:: latex
    
         % Set up the appendix mode and modify the LaTex toc behavior
         \appendix
         %\noappendicestocpagenum
         %\addappheadtotoc
         %\settocdepth{chapter}

.. toctree::
    :maxdepth: 2
    
    priloha-a
    priloha-b
    priloha-c
    priloha-d
    priloha-e
    priloha-f
    priloha-g

