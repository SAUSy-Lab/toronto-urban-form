# Urban Form Toronto

Generating various measures of urban form / built environment / walkability for the Toronto region (i.e. the Greater Golden Horseshoe) from open data sources (e.g. OpenStreetMap, Statistics Canada).

Measures are linked to a hexagonal grid with an apothem of 100m (i.e. 200m between centroids) `output_hex_data`

From this grid, the data has also been interpolated to 2016 Dissemenation Areas (DA) and 2016 Traffic Analysis Zones (TAZ) `output_polygon_data`. 

Everything is constructed using PostGIS, python, and a few command line utilities.

## Summary of Urban Form Measures:

Source data is linked to the hex grid via areal interpolation (for polygon and linear data) or using a spatial join (for point data). See the python notebooks for details on how each measure was generated. The following are the measures generated thus far.

`
pop2016, 2016 population density (from census)
emp2016, 2016 employment density (from census)
business2016, 2016 business density (from Canadian business registry)
int3way, number of 3-way intersections (from OSM)
int4way, number of 4-way or more intersections (from OSM)
transit_n_per_hour, number of transit trips per hour which serve bus stops in the area (from various GTFS)
walk_edge_length, total length of the walking network (from OSM)
`

Population Density

![](imgs/img_population.png)

Employmet Density

![](imgs/img_employment.png)

Business/Store Density

![](imgs/img_business.png)

Transit Trip Frequency

![](imgs/img_transit.png)

Walking Network Density

![](imgs/img_edge.png)

Street Intersection Density (number of 3way and 4+way intersections)

![](imgs/img_intersections.png)

