# Urban Form Toronto

Generating various measures of urban form / built environment / walkability for the Toronto region (i.e. the Greater Golden Horseshoe) from open data sources (e.g. OpenStreetMap, Statistics Canada).

Measures are linked to a hexagonal grid with an apothem of 100m (i.e. 200m between centroids). From this grid, they can be interpolated to other commonly used geomtric units (e.g. Census Tracts, Traffic Analysis Zones, etc.)

Everything is constructed using PostGIS, python, and a few command line utlities.

## Summary of Urban Form Measures:

Population Density

![](imgs/img_population.png)

Employmet Density

![](imgs/img_employment.png)

Business/Store Density

![](imgs/img_business.png)

Transit Trip Frequency

![](imgs/img_transit.png)

Source data is linked to the hex grid via areal interpolation (for polygon data) or using a spatial join (for point data). See the python notebooks for how the data was generated.

Still to come are measures of intersecion and network density.
