Příloha E: Geometrická validita geoprvků
========================================

U dat poskytovaných veřejnou správou se obvykle předpokládá určitá míra jejich
návaznosti. Proto je nezbytné, aby data byla po geometrické stránce validní, a
to i proto, že existuje velice úzká souvislost mezi validitou dat a jejich
jednoznačností. Jinak řečeno, validní data nemohou být po geometrické stránce
dezinterpretována a budou v různých softwarech zobrazena vždy stejně. Za
geometricky validní data považujeme taková data, která jsou v souladu se
specifikací OGC Simple Features [ref51]_.

Obzvláště u prostorových dat exportovaných ze systémů, nesloužících primárně
jako geografické informační systémy, jako je například CAD, můžeme nezřídka
najít chybné geometrie. Nejčastější chybou bývají nesprávně "zaplochované"
polygony, zdvojené hranice mezi dvěma polygony, překřížené hranice sousedících
ploch a další chyby v topologii. Výsledkem bývá například chybný výpočet plochy,
který  neodpovídá skutečné ploše popisovaného jevu.

K tomuto problému můžeme přistupovat z různých pohledů. V ideálním případě
pořizujeme data způsobem, který vylučuje jejich uložení v případě, že nejsou po
geometrické stránce v pořádku. Na druhou stranu to není vždy technicky možné.
Často pracujeme s přebíranými daty, kde by bylo pro jejich vyčištění do nich
nutné neúměrně zasáhnout. To však není vždy možné. Platí zde přímá úměra, čím
jsou data závaznější, důležitější, tím obtížnější bývá jejich čištění. V takovém
případě není vždy možné poskytovat data dokonale validní a korektní. V takové
situaci je třeba spolu s daty udržovat aparát pro popis chyb a u jednotlivých
záznamů uvádět, zda jsou plně validní. Příkladem tohoto přístupu mohou být data
o ZCHÚ a NATURA poskytovaná AOPK. Vhodnou formou se zdá být záznam o chybách v
metadatech.

