---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
---

In the following, I collect some interesting real-world datasets in spatial databases.

## Road Networks
These real-world road networks were extracted from **OpenStreetMap** on Feb. 2021, based on the processing method in our VLDB'18 paper.
If you want to use the road networks below, please consider citing this homepage and our VLDB'18 paper ([BibTex](https://dblp.uni-trier.de/rec/journals/pvldb/TongZZCYX18.html?view=bibtex)).
Briefly speaking, the datasets are obtained based on the following steps.
1. We download region/country .osm from [Geofabrik](http://download.geofabrik.de/index.html), which maintains the OpenStreetMap data
2. We extract the exact .osm based on the corresponding .poly via [Osmconvert](https://wiki.openstreetmap.org/wiki/Osmconvert)
3. We extract the graph files based from the corresponding .osm via [OsmToRoadGraph](https://github.com/AndGem/OsmToRoadGraph)
Notice, in these graphs, the unit of distance is meter and the unit of travel time is second.
If you want to do shortest distance/path queries on these graphs, I think the VLDB'18 paper named "An Experimental Study on Hub Labeling based Shortest Path Algorithms" from Ye Li et al. could be very useful (see their paper for more details).
I have revised their source code to fit the double-type of edge weights ([[Our Code](https://github.com/BUAA-BDA/sspexp_clone)]).
 
| Name             | Description   | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ------        | ---------- | ------- | -------------- | ----------------- | ----------- |
| USA              | Full USA      | 23,947,347 | 23,947,347 | [XXX](#)    | [XXX](#)          |  [XXX](#)   |
| USA              | Full USA      | 23,947,347 | 23,947,347 | [XXX](#)    | [XXX](#)          |  [XXX](#)   |
| USA              | Full USA      | 23,947,347 | 23,947,347 | [XXX](#)    | [XXX](#)          |  [XXX](#)   |

