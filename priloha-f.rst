Příloha F: Kódování češtiny
===========================

Dříve poměrně rozšířeným nešvarem u dat vydávaných státní správou, který v
současnosti naštěstí již téměř vymizel, bylo občas velmi svévolné nakládání s
kódováním češtiny. Obvyklou příčinou bylo využívání datového typu nvarchar v databázi,
který umožňoval do jedné položky ukládat data v různých kódováních. Při
kombinaci dat z historicky různých zdrojů zůstával tento problém zakonzervován
přímo v databázi. Při výdejích dat ve formátech jako je DBF (v rámci formátu
Esri Shapefile), MS Excel, MDB soubory databáze MS Access a podobně vznikaly
situace, kdy bylo velmi obtížné data importovat do cílového prostředí bez ruční
opravy. Pro automatizované zpracování publikovaných dat je proto nezbytné, aby
kódování bylo stejné u všech souborů. Ideální volbou je UTF-8.
