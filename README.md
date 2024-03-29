# WebmapsImmi

A collection of webmaps and charts on immigration.
Link: http://thomashe89.github.io/WebmapsImmi/

## Workflow

#### Choropleth maps on asylum applications (abs/rel)
1. Download world shapefile/geoJSON from the web (e.g. from [thematicmapping](http://thematicmapping.org/downloads/world_borders.php))
1. Delete unnecessary columns (features): 
	- convert to ESRI shape file
	- toggle editing
	- use click-based deletion of features
1. Download number of asylum applications and total population (both by country, 2008-2015) from Eurostat
1. Do some preprocessing in R and save the pop/immi data as csv (mergeData.csv)
1. Join in QGIS and export as geoJSON (alldata.geojson)
	- right-click on layer in layers panel -> Properties -> Joins
	- right-click on layer in layers panel -> Save as... -> under Format, select geoJSON 


#### ZEIT article replication
1. Here is the [article link](http://www.zeit.de/politik/deutschland/2015-11/anti-immigrant-violence-germany)
1. Download [replication data](https://docs.google.com/spreadsheets/d/1yxi3oV96kxag_3GiVnGvndgJ5zTI-lHsaAB-p7U-g3w/edit#gid=1734573181) and convert to csv (attacks.csv).  
1. Use Python (GetCoord.ipynb) to get coordinates since spreadsheet does **not** contain latlng (attacks_final.xlsx).
1. Steal incident type icons from original map (cf. article).
1. Use R to translate data set, summarize state of investigation, count within states, and make graphics.
1. Add new layers to map: incident type, state of investigation, summary per state.

#### Make one more map (deaths and routes)?
