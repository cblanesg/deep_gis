# deep_gis: Patterns

The purpose of this repo is to include a set of tools and examples of **Geographic Information Systems** (GIS) useful for developers. This repo provdes various scenarios that the user might enocunter while using georeferenced data.


# Content

The following table is a summary of all the files included in this section, below is a brief explanation of each scenario.

| Scenario | Description | File | Data|
|----------|-------------|------|-----|


# Why identify geographic patterns?

Any distribution of features or attribute values within a defined area will create a pattern. Geographic patterns range from completely clustered at one extreme to completely dispersed at the other. A pattern that falls at a point between these extremes is said to be random. Knowing if there's a pattern in your data is useful if you need to gain a better understanding of a geographic phenomenon, monitor conditions on the ground, compare patterns, or track changes. 

## Using statistics to identify patterns
One way to identify patterns in you geographical data is:
1. Display the features or values in the map. 
2. Use statistics to measure the extent to which features or values are clustered, dispersed, or random. You compare the actual distribution of features to a hypothetical random distribution of the same number of features over the same area. The GIS calculates the statistic for te observed distribution as well as what the statistic would be for a random distribution. The extent to which the observed disribution deviates from the random distribution is the extent to which the pattern is more clustered or more dispersed than the random distribution. You state the null hypothesis and then set out to to determine whether to reject it, or not, with some level of confidence. The result of the analysis can be tested to calculate the porbability that a pattern isn't simply due to chance or if it reflects a real pattern. 

1 vs 2: Using statistics to measure a patteren is more accurate, as identifying a pattern with a classification methos or class ranges can affect whether there appears to be a pattern or not.The satistical tool use the underlaying data value ofeach feature, identifiying a pattern odes not depend on how the values are classified and displayed.