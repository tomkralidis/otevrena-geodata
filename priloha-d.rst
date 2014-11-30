Příloha D: Čas a standard WCS 2.0.0
===================================
Níže uvedené příklady předpokládají, že čas je vedle souřadnic X,Y veden jako další rozměr dat. Čas je zadáván v souladu s technickou normou ISO 8601.

Příklad požadavku WCS s časovým omezením - Key Value Pairs
----------------------------------------------------------

::

    http://www.myserver.org:port/path?service=WCS&version=2.0&request=GetCoverage
    &coverageId=C0002 
    &subset=long(100,200)
    &subset=lat(50,60)
    &subset=days("2009-11-06T23:20:52Z","2009-11-06T23:20:52Z")

Příklad požadavku WCS s časovým omezením - XML POST
---------------------------------------------------

.. code-block:: xml

    <gmlcov:GridCoverage ... gml:id="C0001"> 
       <gml:boundedBy>
            <gml:Envelope srsName="http://www.opengis.net/def/crs-compound?
                                   1=http://www.opengis.net/def/crs/EPSG/0/4326&
                                   2=http://www.opengis.net/def/crs/OGC/0/Days“ 
            axisLabels="Lat Long Time" uomLabels="deg deg day" srsDimension=“3">
               <gml:lowerCorner>1 1 2012-03-10</gml:lowerCorner>
               <gml:upperCorner>3 10 2012-03-10 </gml:upperCorner>
            </gml:Envelope>
        </gml:boundedBy>
        ...
    </gmlcov:GridCoverage>

