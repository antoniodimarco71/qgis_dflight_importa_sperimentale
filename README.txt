IMPORT D-FLIGHT UAS GEO ZONES PLUG-IN
--------------------------------------------------------------------

This is an experimental plugin, no liability is assumed for its use

The plug-in has been developped through IA assistance

It has been tested on QGIS 3.40.12-Bratislava

Version: 0.5 - 20260907

--------------------------------------------------------------------

WHAT IS THIS PLUGIN FOR?

This experimental plugin converts the JSON file produced by the D-Flight Italian web portal into a GeoPackage.

It is useful for reporting in vector form all the Italian geographical areas relating to drone flights and categorising them with different colours based on the maximum permitted flight altitudes (see the GML STYL paragraph)


PRELIMINARY OPERATIONS

- obtain the json.gz file from your D-Flight account on D-Flight web application (https://www.d-flight.it/web-app)

- unzip the json.gz file into any folder


THAN FOLLOW THESE STEPS

1) Go to Plug-in menu and choose Importa UAS Geo Zone di Dflight - Importa Zone D-Flight sub-menu

2) Go to the folder containing the JSON file

3) Choose a name and where to save the converted file (only GeoPackage - gpkg is admitted at the moment)

4) The plug-in will automatically popup if the file has been imported, the number of imported geometries, the number of not imported geometries and the log directory

5) Than you will be prompted if you want to open or not the log file

6) Than a QML style will be automatically applied (it's in the styles folder)



NOTE: A log is generated for geometries that cannot be imported and it's saved in the same directory named like "dflight_geozones_yyyymmdd_log.txt"


PAY ATTENTION: At the time of the plugin is released, it seams the JSON file does not include military areas.


Any further plug-in improvement can be sent to the author's e-mail: dimarco71@gmail.com

-------------------------------------------------------


GML STYLE

NOTAM: violet - "name" LIKE '%NOTAM%'
0 m: red - "name" NOT LIKE '%NOTAM%' AND "lowerLimit" = 0
25 m: orange - "name" NOT LIKE '%NOTAM%' AND "lowerLimit" = 25
45 m: yellow - "name" NOT LIKE '%NOTAM%' AND "lowerLimit" = 45
60 m: blue - "name" NOT LIKE '%NOTAM%' AND "lowerLimit" = 60

--------------------------------------------------------

JSON ATTRIBUTE

identifier
country
name
type
restriction
reason
otherreasonInfo
authority_name
authority_email
authority_phone
permanent
lowerLimit
upperLimit
lowerVerticalReference
upperVerticalReference
uomDimensions



