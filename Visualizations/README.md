# deep_gis: visualizations

The purpose of this repo is to include a set of tools and examples of **Geographic Information Systems** (GIS) useful for developers. This repo provdes various scenarios that the user might enocunter while using georeferenced data.


# Content

The following table is a summary of all the files included in this section. 

| Scenario |  Description | File | Data |
|----------|--------------|------|------|
|Choropleth Map | A choropleth map displays divided geographical areas or regions that are **coloured in relation to a numeric variable**. It is useful when you want to study how a variable evolutes along a territory| choropleth_map.ipynb | Shapefiles China, Coronavirus Cases (https://github.com/CSSEGISandData/COVID-19)|
| Bubble Map  | A bubble map uses **circles of different size to represent a numeric value on a territory**. It is possible to display a bubble per geographic coordinate, or a bubble per region (in this case the bubble is usually displayed in the baricentre of the region). It is useful to avoid the bias caused by regional area sizes in choropleth maps.| ||
 |Connection Map  | A connection map allows to show the connection between several positions on a map. The link between 2 places can be drawn with a straight line, or more commonly by representing the ‘great circle‘: the shortest route between them. Knowing that the earth is a sphere, this results in rounded lines that give a really pleasant look to the map.| ||
| Hexbin map | A hexbin map splits a geographic area in a multitude of hexagons. A numeric value is attributed to each hexagone, what controls its color. Hexbin map is a kind of choropleth map. Itis useful to remove the bias introduced by the different region size in choropleth, since each region is represented by the same hexagone.| ||
