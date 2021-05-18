# deep_gis: spatial data toolkit

The purpose of this repo is to include a set of tools and examples of **Geographic Information Systems** (GIS) useful for developers. This repo provdes various scenarios that the user might enocunter while using georeferenced data.


# Content
The structure of the repo is organized in the following sections:
1. Pre-Processing Spatial Data 
2. Visualization
3. Spatial Measurements and Statistics
4. Data

Each section is provided with a set of relevant scenarios that the developer might encounter, each scenario is provided with relevant functions and end-to-end examples (demonstrated in Jupyter notebook). 

## Pre-Processing Spatial Data

The Data Structure used for spatial data are **GeoDataFrame** or **GeoSeries**. These are subclasses of pandas Series and DataFrame, respectively. Both objects may contain a column or a vector with geometrical (shapely) objects. This geometrical objects can be:
1. Point - ex. a point in a map (referenced on a coordenate )
2. Polygon - ex. area of a map like a state (referenced by a set of vectors associated with coordinates)
3. LineString - ex. route (referenced by a set of coordinates)

There are many different vector-based spatial data, that includes a geometry object, like: ESRI shapefile or GeoJSON files. Many libraries in Pyhton can read this type of data, for example: *geopandas*. 

### Vector-based spatial data

#### Shapefile
A shapefile is a vector-based spatial data. They are simple storage formats that allow to create georeferenced geometry (Points, Polygons, LineStrings). One shapefile must have *at least* 3 files (most shapefiles have around 6 files):
1. .shp - this file stores the geometry of the feature
2. .shx- this file stores the index of the geometry
3. .dbf - this file store the attribute information for the feature

All files **must** be stored in the same location with the same name or else the shapefile will not load. 

#### GeoJSON
GeoJSON is a format for encoding a variety of geographic data structures. This type of file supports geometry types such as: Point, LineString, Polygon, MultiPoint, MultLineString and MultiPolygon. Geometric objects with additional properties are **Feature** objects (is the equivalent to de .dbf file in the shapefile format). Sets of features are contained by *FeatureCollection* objects. The GeoJson have the same information of a shapefile but it is stored in a different way. 

Example of a GeoJSON:

`{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  },
  "properties": {
    "name": "Dinagat Islands"
  }
}`

### Coordinate Reference Systems
All vector- based spatial data is referenced to a Coordinate Reference System (CRS). The CRS is important because the geometric shapes in vector- based spatial data are simply a collection of coordinates in an **arbitrary space**. A CRS tells Python how those coordinates relate to places on the Earth. The following figures show different Coordinate Reference Systems:

![image](https://github.com/cblanesg/gis/blob/master/crs.png)

`When you work with more than one vector- based spatial data you must asure that they are in the same CRS, otherwise you will not be able to associate the databases. `


### Content Pre-Processing Data

The following table is a summary of the scenarios covered in this section.

|Scenario | Description | 
|---------|-------------|
| Load vector-based spatial data| Load and project GeoJSON files and shapefiles in bokeh. |  
| Transform csv with coordinates points to a GeoDataFrame | | 
| Change CRS from a shapefile + merge spatial data with different CRS's.| | 


## Spatial Measurements and Statistics

This section is divided into three categories:
1. Descriptive Statistics: focused on geographic distributions. 
2. Patterns: identifying patterns of geographic features
3. Clusters:  identifying spatial clusters (includes algorithm of spatial-temporal cluster)
4. Geographic Relationships

The following table is a summary of the scenarios covered in each category. 


| Scenario  | Use | Description of Section | 
|-----------|-------------|-----|
| Descriptive Statistics | Identifying the distribution of a set of spatial features can give you insights into the phenomenon of interest | In this section will be covered: measurement of the distribution of a set of features, which allows you to calculate a characteristic of the distribution, such as its **center compactness, orientation** or **direction** | 
| Patterns | Identifying the pattern created by a set of features allows you to gain a better understanding of the distribution of features, monitor conditions, compare different features, or track changes | In this section will be covered:  statistics to identify patterns, measure the pattern of feature locations and measure the spatial pattern of feature values. |
| Clusters | Identifying clusters allows you to map hot spots and cold spots. By comparing the clisters to the locations of other features you can better understand why the clusters occur and decide what action to take. |In this section will be covered: satistics to identify clusters, finding clusters of features, finding clusters of similar values and spatial temporal clusters. | 
| Geographic Relationships | Analyzing the realtionships between geographic phenomena gives you a better understanding of what's happening in a location, lets you predict where something might occur, and helps you examine why things occur where they do| In this section will be covered: statistics to analyze relationships, identifying geographic relationships and analyzing geographic processes. |


## Visualization
The following table is a summary of the scenarios covered in this section. 

| Scenario |  Description | 
|----------|--------------|
|Choropleth Map | A choropleth map displays divided geographical areas or regions that are **coloured in relation to a numeric variable**. It is useful when you want to study how a variable evolutes along a territory| 
| Bubble Map  | A bubble map uses **circles of different size to represent a numeric value on a territory**. It is possible to display a bubble per geographic coordinate, or a bubble per region (in this case the bubble is usually displayed in the baricentre of the region). It is useful to avoid the bias caused by regional area sizes in choropleth maps.| 
 |Connection Map  | A connection map allows to show the connection between several positions on a map. The link between 2 places can be drawn with a straight line, or more commonly by representing the ‘great circle‘: the shortest route between them. Knowing that the earth is a sphere, this results in rounded lines that give a really pleasant look to the map.|
| Hexbin map | A hexbin map splits a geographic area in a multitude of hexagons. A numeric value is attributed to each hexagone, what controls its color. Hexbin map is a kind of choropleth map. Itis useful to remove the bias introduced by the different region size in choropleth, since each region is represented by the same hexagone.| 
| Sankey Diagrams | Allows to display flows. several entities (nodes) are represented by rectangles or text. Their links are represented with arrow or arcs that have a width proportional to the importance of the flow. Are used to show weighted networks (i.e. **flows**) |

## Data

All the data used in the examples are included, as well as other data that may be useful for the developer. 

 
