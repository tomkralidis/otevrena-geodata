.. index::
    pair: Atom; Formát Atom

.. _atom-priloha:

Příloha G: Formát Atom
======================
Atom (Atom Syndication Format) je webový standard pro publikování
syndikovaného obsahu. Je nástupcem
populárního formátu RSS (který nikdy zcela nevytlačil).

Samotný kanál a jednotlivé jeho položky musí mít uvedený název, jedinečný
identifikátor (URI) a datum poslední změny. Data (text, XML či binární data)
mohou být přímo součástí kanálu, to ovšem pro geodata není z pochopitelných
důvodů vhodné a proto je lepší uvézt odkaz (`link`) na datovou sadu.

Níže uvádíme *hypotetický* příklad kanálu ve formátu Atom, který obsahuje 3
položky, a to vrstevnice s přesností 1, 2 a 5 metrů.

.. code-block:: xml

    <?xml version="1.0" encoding="utf-8"?>
    <feed xmlns="http://www.w3.org/2005/Atom">

      <title>Otevřená data IPR Praha</title>
      <link href="http://geoportalpraha.cz"/>
      <link href="http://geoportalpraha.cz/opendata/feed" rel="self"/>
      <updated>2015-01-01T12:00:00+0100</updated>
      <author>
        <name>Josef Novák</name>
        <email>josef.novak@iprpraha.cz</email>
      </author>
      <id>ipr:data.urm.cz:2B7AB7CF-A6B0-4AB8-BB2B-229AC168605C</id>

      <entry>
        <title>Vrstevnice 1 m</title>
        <link href="http://geoportalpraha.cz/data/vrstevnice_1m.gpkg"/>
        <id>CZ-URM-MAP.MAP_vrstevnice_1m_l</id>
        <updated>2010-12-16</updated>
        <summary>Vrstevnice jsou vygenerované z Digitálního modelu terénu 2010.
                 Vrstevnicový plán odpovídá obsahem a přesností úrovni map 1:5000.
                 Přesnost cca 1m.
        </summary>
      </entry>

      <entry>
        <title>Vrstevnice 2 m</title>
        <link href="http://geoportalpraha.cz/data/vrstevnice_2m.gpkg"/>
        <id>CZ-URM-MAP.MAP_vrstevnice_2m_l</id>
        <updated>2010-12-16</updated>
        <summary>Vrstevnice jsou vygenerované z Digitálního modelu terénu 2010.
                 Vrstevnicový plán odpovídá obsahem a přesností úrovni map 1:5000.
                 Přesnost cca 2m.
        </summary>
      </entry>
      
      <entry>
        <title>Vrstevnice 5 m</title>
        <link href="http://geoportalpraha.cz/data/vrstevnice_5m.gpkg"/>
        <id>CZ-URM-MAP.MAP_vrstevnice_5m_l</id>
        <updated>2010-12-16</updated>
        <summary>Vrstevnice jsou vygenerované z Digitálního modelu terénu 2010.
                 Vrstevnicový plán odpovídá obsahem a přesností úrovni map 1:5000.
                 Přesnost cca 5m.
        </summary>
      </entry>

      <!-- ... Další záznamy ... -->
    </feed>


