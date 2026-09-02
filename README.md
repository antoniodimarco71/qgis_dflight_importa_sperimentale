# qgis_dflight_import_experimental
Importa in Qgis le Geo Zone scaricate da D-Flight

-------------------------------------------------------
# DISCLAIMER
Experimental plugin;
no liability is assumed for its use.
-------------------------------------------------------

This experimental plugin converts the JSON file produced by the D-Flight portal into a GeoPackage.

Steps to follow

PRELIMINARY: obtain the json.gz file from the D-Flight portal THAN

1) Unzip the json.gz file downloaded from D-Flight into any folder
2) Launch the plugin and navigate to the folder containing the JSON file
3) Choose where to save the converted file
4) In QGIS apply the QML style associated with the plugin in the styles folder

   NOTE: A report is generated for geometries that cannot be imported.
   PAY ATTENTION: At the time of the plugin's release, the JSON file does not include military areas. Any further improvements are welcomed and can can be sent to: a.dimarco@arpat.toscana.it
