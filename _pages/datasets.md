---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
---

In the following, I collect some interesting real-world datasets in spatial databases.

## Overview
* [Road Networks](#Road-Networks)
* [Urban Logistics](#Urban-Logistics)


## Road Networks
These real-world road networks were extracted from **OpenStreetMap** on Feb. 2021, based on the processing method in our VLDB'18 paper.
If you want to use the road networks below, please consider citing this homepage and our VLDB'18 paper ([BibTex](https://dblp.uni-trier.de/rec/journals/pvldb/TongZZCYX18.html?view=bibtex)).
Briefly speaking, the datasets are obtained based on the following steps.

1. We download region/country .osm from [Geofabrik](http://download.geofabrik.de/index.html), which maintains the OpenStreetMap data
2. We extract the exact .osm based on the corresponding .poly via [Osmconvert](https://wiki.openstreetmap.org/wiki/Osmconvert)
3. We extract the graph files based from the corresponding .osm via [OsmToRoadGraph](https://github.com/AndGem/OsmToRoadGraph), where the road network type is car

Notice, in these graphs, the unit of distance is meter and the unit of travel time is second.
If you want to do shortest distance/path queries on these graphs, I think the VLDB'18 paper named "An Experimental Study on Hub Labeling based Shortest Path Algorithms" from Ye Li et al. could be very useful (see their paper for more details).
I have revised their source code to fit the double-type of edge weights ([our code](https://github.com/BUAA-BDA/sspexp_clone) is here).
 
### USA 
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| California | 16,129,269 | 34,333,910 | [Cali*.road-d, 864 MB](/California.road-d.tar.gz) | [Cali*.road-t, 845 MB](/California.road-t.tar.gz) | [Cali*.co, 338 MB](/California.co.tar.gz) |
| Florida | 9,303,268 | 20,249,786 | [Flor*.road-d, 493 MB](/Florida.road-d.tar.gz) | [Flor*.road-t, 482 MB](/Florida.road-t.tar.gz) | [Flor*.co, 186 MB](/Florida.co.tar.gz) |
| Newyork | 6,959,649 | 14,675,944 | [Newy*.road-d, 357 MB](/Newyork.road-d.tar.gz) | [Newy*.road-t, 348 MB](/Newyork.road-t.tar.gz) | [Newy*.co, 139 MB](/Newyork.co.tar.gz) |
| Colorado | 5,118,452 | 10,799,592 | [Colo*.road-d, 261 MB](/Colorado.road-d.tar.gz) | [Colo*.road-t, 255 MB](/Colorado.road-t.tar.gz) | [Colo*.co, 107 MB](/Colorado.co.tar.gz) |


### China 
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| California | 16,129,269 | 34,333,910 | [Cali*.road-d, 864 MB](/California.road-d.tar.gz) | [Cali*.road-t, 845 MB](/California.road-t.tar.gz) | [Cali*.co, 338 MB](/California.co.tar.gz) |
| Florida | 9,303,268 | 20,249,786 | [Flor*.road-d, 493 MB](/Florida.road-d.tar.gz) | [Flor*.road-t, 482 MB](/Florida.road-t.tar.gz) | [Flor*.co, 186 MB](/Florida.co.tar.gz) |
| Newyork | 6,959,649 | 14,675,944 | [Newy*.road-d, 357 MB](/Newyork.road-d.tar.gz) | [Newy*.road-t, 348 MB](/Newyork.road-t.tar.gz) | [Newy*.co, 139 MB](/Newyork.co.tar.gz) |
| Colorado | 5,118,452 | 10,799,592 | [Colo*.road-d, 261 MB](/Colorado.road-d.tar.gz) | [Colo*.road-t, 255 MB](/Colorado.road-t.tar.gz) | [Colo*.co, 107 MB](/Colorado.co.tar.gz) |


## Urban Logistics
