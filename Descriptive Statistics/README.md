# deep_gis: descriptive statistics

The purpose of this repo is to include a set of tools and examples of **Geographic Information Systems** (GIS) useful for developers. This repo provdes various scenarios that the user might enocunter while using georeferenced data.


# Content

The following table is a summary of all the files included in this section, below is a brief explanation of each scenario.

| Scenario | Description | File | Data|
|----------|-------------|------|-----|
| Central Feature | In this notebook it is shown how to find the mean, the median and a Central Feature from a group of features| Geometric_Median_and_Feature.ipynb | Buildings in CDMX |
| Measuring Compactness | The objective is to obtain a measure of the copactness of the data | compactness.ipynb | Buildings in CDMX|
| Measuring Orientation | The objective is to obtain a measure of the orientation of the data| measuring_orientation.ipynb |  Open Spaces in CDMX and Comercial business in CDMX |
| Measuring Direction | The obkective of this notebook is to examin the street etwork orientation of different Mexican States (Aguascalientes, Jalisco, Nuevo León, Oaxaca). Each state is representted by a polar histogram (rose diagram) depicting how its streets orient. Each bar'sdirection represents the compass bearings of the streets and its length representes tge realtive frequency of streets with those bearings. | measuring_direction.ipynb | Data from osmnx library (code obtained from https://geoffboeing.com)|

## Central Feature

There are three kinds of center:
1. Central Feature: It is the average x-coordinate and average y-coordinate for all features in the study area. *It is good to track changes or compraing distributions*.
2. Median Center: The x,y coordinate having the shortest distance to all features in the study area. *It is good for finding the most accesible location*. 
3. Mean Center: The feature having the shortest total distance to all other features in the study area. *It is good for finding the most accesible feature*. 

`The difference between the Median and the Mean Center is that the result of the Median is a point that is not necessarily in your data set and the Mean Center returns a point from your data set.`

## Compactness

Measuring compactness of a distribution provides a single value representing the dispersion of features around the center. The value is a distance, so the **compactness** can be represented on a map by drawing a circle with the radius equal to the value. The compactness measures the *average distance the features vary from the mean center*. It is the same as the standard distance deviation or simply standard distance. 

## Direction and Orientation

Measuring orientation and direction let you abstract the spatial trends in a distribution of features. By calculating the orientation of a group of a set of points, the analyst could see a pattern of the behaviour of the data. 

To measure the **orientation** you usually the variance separately for the x-coordinates and the y-coordinates. These twoe measures deine the axes of an ellipse encompassing the distribution of features. The ellipse allows you to see if the distribution of features is elongated and hence has a particular orientation. 