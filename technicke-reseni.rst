.. index::
    single: Technické řešení

Technické řešení infrastruktury otevřených dat
==============================================

Při návrhu a budování infrastruktury otevřených dat je vhodné dodržovat několik
základních pravidel, která zabezpečí maximální efektivitu, rozšiřitelnost a
odolnost celého řešení.

* Vnitřní infrastrukturu je nutné logicky, ne nutně fyzicky, oddělit od
  infrastruktury pro poskytování otevřených dat
* Data jsou publikována v souladu s platnými standardy. Je možné, že stávající
  softwarové vybavení nebude tuto podmínku splňovat. Softwarové řešení může být
  hybridní (open source vs. propritary), každopádně takové, aby plnilo daný
  účel.
* Pokud to licenční podmínky umožní, je vhodné v maximální míře využít
  stávajících technologií tak, aby se zbytečně nerozšiřovalo spektrum
  provozovaného software a tím i složitost celého řešení. To znamená, že
  optimální je vnitřní infrastrukturu geografických dat a infrastrukturu dat
  otevřených provozovat na stejné platformě, doplněné o případné nutné další
  technologie tam, kde fyzicky stávající technologie nedostačuje.
* Klíčovým prvkem infrastruktury je validace dat před jejich publikováním.
  validátor příslušného standardu. Validaci samotnou je nutné svěřit jiné části
  týmu, případně externistům, aby byly nalezeny i nepopsané vlastnosti, sdílené
  pouze vnitřními pracovníky.
* Provoz dynamických služeb je vhodné delegovat na externí infrastrukturu, která
  umožní zabezpečit její škálovatelnost a dostupnost podle aktuálního zatížení

.. figure:: imgs/technicke-reseni.png
   :scale: 100 %
   :alt: Schéma technické infrastruktury
   :align: center
   
   *Technická infrastruktura při otevírání dat*



Nasazené řešení je vhodné testovat na co možná nejširší škále běžně používaných
nástrojů z oblasti desktopových GIS aplikací, geodatabází, katalogů a pod. Výběr
referenčního softwaru je vždy ovlivněn osobní preferencí administrátora,
objektivními vlastnostmi, znalostí určitého technologického okruhu. 

.. index::
    single: Validace

Doporučení k validaci
---------------------

Publikovaná data v souborových formátech i webové služby by mělo jít snadno
přidat jako vrstvy do tzv. projektů (workspace) v desktopových aplikacích jako
je Esri ArcGIS, GeoMedia, QGIS, případně Topol a další. Pro ověření správnosti
definice souřadnicového systému poskytovaných dat lze použít transformační
nástroje Open Source knihovny GDAL [ref59]_. Dále je pomocí této knihovny vhodné
ověřit konzistenci a validitu dat včetně nastavení kódování češtiny v
poskytovaných datech. To je možné zpětným importem a porovnáním s původními
daty. Knihovna GDAL je taktéž využívána systémem ArcGIS firmy Esri, lze ji tedy
považovat za vhodnou referenční knihovnu. Pro úplnost dodáváme, že za
ekvivaletní řešení ke knihovně GDAL pro prostředí jazyka Java lze považovat
knihovnu GeoTools [ref63]_.

Provázání mezi metadatovým katalogem a samotnou službou je vhodné testovat
pomocí zásuvného modulu QGIS MetaSearch [ref58]_, který umožnuje v katalogu přidat
službu jako vrstvu do projektu. Dále by mělo být možné ověřit validitu služeb
(vyhledávacích ale i prohlížecích a stahovacích) a dat na národním geoportálu
INSPIRE [ref61]_.

Pro automatické testování validity a dostupnosti webových služeb můžeme s
výhodnou využít knihovnu OWSLib [ref62]_, kterou lze spouštět periodicky na serveru
a provádět tak pravidelnou kontrolu.

U poskytovaných geodat, kde předpokládáme migraci na straně uživatele do
geodatabáze, jakou jsou například objemnější data v relační nebo stromové
struktuře, případně soubory se změnovými větami, je na místě tuto migraci
otestovat. Pakliže se zaměříme na Open Source řešení, tak se jako nejvhodnější
referenční geodatabáze jeví PostGIS [ref60]_. Zde je třeba počítat s tím, že postup
nebude triviální a není od věci jej publikovat, například na stránkách IPR. 

Pro ověření funkčnosti a dostupnosti webových služeb, ale i předgenerovaných
rastrových dlaždic prostřednictvím služby OGC WMTS, je vhodné využít i webové
aplikace, např. pomocí knihoven Leaflet [ref64]_ nebo OpenLayers [ref65]_.



