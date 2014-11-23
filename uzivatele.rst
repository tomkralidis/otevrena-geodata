Typické skupiny uživatelů otevřených geodat
===========================================
Uživatele lze obecně dělit podle různých kritérií: na základě schopností,
zkušeností, specializace, požadavků na data a dalších. Tato kritéria jsou
vzájemně provázána, proto se nevyhneme zjednodušení na modelové skupiny
uživatelů.

Pro otevírání geografických dat se jako klíčové jeví tyto skupiny uživatelů:

* Uživatel mapového portálu
* Běžný uživatel Geografického informačního systému (GIS)
* Specialista GIS (geoinformatik)
* Datový analytik (mimo obor GIS)
* Programátor/vývojář

Uživatel mapového portálu
-------------------------

Největší částí uživatelů geografických dat je laická veřejnost, která využívá
některý z mapových portálů, případně specializované nástroje pro práci s mapou.
Tato skupina uživatelů není přímo cílovou skupinou otevírání geografikcých dat,
informace se k nim povětšinou dostanou zprostředkovaně právě pomocí portálu,
který využívají. Potřeby a očekávání těchto uživatelů bereme v úvahu zejména při
propagaci otevřených dat.

Běžný uživatel Geografického informačního systému (GIS)
-------------------------------------------------------

Tento typ uživatele obvykle zvládá řešení základních, až středně obtížných úloh
s využitím desktopového GIS, případně nástroje na tvorbu výkresů CAD (AutoCAD,
Microstation apod). Je schopen pracovat s daty, která lze snadno připojit nebo
jednoduše importovat v konkrétním programu, se kterým pracuje. S komplexnějšími
formáty a datovými sadami si obvykle poradí pouze tehdy, pokud se dají otevřít
nástrojem integrovaným do tohoto programu. Data, která sám nevytváří používá
obvykle jako podkladová, případně pro provádění analýz, často jednorázově. Jeho
zájmem jsou tedy spíše data platná k určitému datu, než data průběžně udržovaná
v aktuálním stavu z webové služby.

Příkladem tohoto typu uživatele jsou studenti negeoinformatických oborů, vědci,
tvůrci studií, odborníci vytvářející tematická data, plány či mapy (např. lesní
plány), stavebníci, architekti, pracovníci
ochrany přírody a další odborníci, kteří využívají GIS jako jeden z více
pracovních nástrojů.

Obecně lze tuto skupinu uživatelů považovat za poměrně konzervativní, GIS není
jejich primárním zaměřením, obvykle se jednorázově naučí základům problematiky a
své znalosti dále příliš nerozvíjí. Dalším omezením, zejména pokud využívají
proprietární software, může být využívání starých verzí, které ještě nemají
podporu novějších formátů.

Pro rastrová data je pro tuto skupinu uživatelů ideální využívat data pomocí
služeb Web Map Service (WMS), případně Web Map Tiled Service (WMTS). U
vektorových dat je nejvhodnější stahování jednotlivých vrstev v nějakém
rozšířeném souborovém formátu (např. Esri Shapefile či OGC GeoPackage).
Použití Web Feature Services (WFS) je ideální cílový stav, ale může být
problematické při větších objemech dat, který může uživatel (i když ne
zcela vědomě) po serveru požadovat. Služba OGC WFS umožňuje odpověď "stránkovat", 
což bohužel není na všech klientských programech běžně implementováno.

Specialista GIS (“datař”, geoinformatik)
----------------------------------------

Specialista GIS je odborníkem pro práci s geografickými daty, který preferuje
ucelenou datovou sadu včetně popisných informací, zajímá se o aktuálnost a
přesnost dat. Nemá problém vybrat z nabídky tu, která nejvíce odpovídá jeho
potřebám. Kromě pokročilých analýz a vizualizací připravuje datové sady pro
použití v rámci organizace jak pro vnitřní informační systémy, tak pro méně
zkušené uživatele.

Překážkou, se kterou se u GIS specialistů někdy setkáváme, je přílišná vazba na
konkrétní software, se kterým pracují. Specialisté se vyhýbají použití nového,
pro ně neznámého software a nebo jsou v situaci, že jim zaměstnavatel či
pracovní podmínky či oborové zvyklosti neumožní alternativní software využívat.

Obvykle si budují své databáze, ve kterých se snaží udržovat aktuální kopii
celých datových sad, což umožňuje provádět rychlé a komplexní analýzy nad
velkými daty. Poskytují webové služby s vysokou dostupností dimenzované pro
potřeby konkrétních aplikací. Pro udržování aktualizované datové sady je
nejvýhodnějším způsobem distribuce poskytování stavových dat a změnových vět,
ideálně opatřených kvalitními metadaty ve standardním formátu. V případě
poskytování dat touto cestou je potřeba, aby bylo umožněno automatizované
vytěžování dat, tedy umísťování souborů na odvoditelné adrese nebo předávání
odkazy na soubory ke stažení.

Datový analytik
---------------
Další skupinou uživatelů je odborník na analýzu dat bez zázemí GIS. Jelikož
nezná běžně se vyskytující datové formáty ani pravděpodobně nemá k dispozici
potřebný software, bývá odkázán na vlastní nástroje (nejčastěji databáze a
statistické softwary), pomocí nichž data zkoumá.

Datový analytik tedy potřebuje formát otevřený, ideálně textový, dobře
dokumentovaný. Práci usnadní zejména formalizované popisy dat, jako jsou například XSD
schémata, která se používají při  generování různých šablon pro dokumenty XML,
připojení dat apod.

Ideálním způsobem distribuce jsou pro něj předgenerované soubory v textovém
strukturovaném formátu (JSON, XML, ...), ale je schopen, pokud je dostupná
uživatelská dokumentace, využít i webové služby.


Programátor/vývojář
-------------------

Přestože skupina vývojářů není příliš početná, je velice důležitá. Vývojáři
totiž zpřístupňují data pomocí aplikací, obvykle vyvinutých na míru specifickým
cílům nebo tematickému okruhu uživatelů. Kvalita popisu  formátu a dostupnost
knihoven pro jejich využití značně ovlivňuje náklady, se kterými tyto aplikace
vznikají. Přestože sami jsou vývojáři často skalními zastánci různých
technologií (.NET, C++, Java atd), geografická data jsou pro ně cizí a akceptují
proto jakýkoli funkční a dobře popsaný standard, nejlépe přímo s knihovnou k
jeho využívání. Důležitým faktorem pro tuto skupinu je také otevřená licenční
politika, tedy možnost poskytnutá data přizpůsobovat konkrétním potřebám. Dále
oceňují stabilitu poskytovaných služeb a dat, protože připravují služby určené k
dlouhodobému využití. Je proto vhodné, aby  data byla poskytována dlouhodobě a
bez zásadních změn.

Vývojáři sledují trendy a vývoj v oboru Informačních technologií (IT), mají
přehled o novinkách a jsou schopni využít výhod nových a zatím nepříliš
rozšířených forem přenosu dat i technologií. Ani komplikovanější formáty pro ně
nemusí být problémem, pokud je dostupná kvalitní dokumentace.

Ideálním způsobem distribuce dat pro takto vymezenou skupinu uživatelů jsou
proto bezesporu webové služby, pokud jsou ovšem stabilní, rychlé a vhodně
nastavené. S jejich využitím velice efektivně vytvoří aplikaci,  aniž by musel
provozovat vlastní server a udržovat na něm aktuální data.
