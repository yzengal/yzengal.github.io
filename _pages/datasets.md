---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
---

In the following, I collect some interesting real-world datasets in spatial databases.

{% include base_path %}
{% include toc %}

## Road Networks
These real-world road networks were extracted from **OpenStreetMap** on Feb. 2021, based on the processing method in our VLDB'18 paper.
If you want to use the road networks below, please consider citing this homepage and our VLDB'18 paper ([BibTex](https://dblp.uni-trier.de/rec/journals/pvldb/TongZZCYX18.html?view=bibtex)).
Briefly speaking, the datasets are obtained based on the following steps.

1. We download region/country .osm from [Geofabrik](http://download.geofabrik.de/index.html), which maintains the OpenStreetMap data
2. We extract the exact .osm based on the corresponding .poly via [Osmconvert](https://wiki.openstreetmap.org/wiki/Osmconvert)
3. We extract the graph files based from the corresponding .osm via [OsmToRoadGraph](https://github.com/AndGem/OsmToRoadGraph), where network type is car

Notice, in these graphs, the unit of distance is meter and the unit of travel time is second.
If you want to do shortest distance/path queries on these graphs, I think the VLDB'18 paper named "An Experimental Study on Hub Labeling based Shortest Path Algorithms" from Ye Li et al. could be very useful (see their paper for more details).
I have revised their source code to fit the double-type of edge weights ([our code](https://github.com/BUAA-BDA/sspexp_clone) is here).
 
### USA 
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| California | 16,129,269 | 34,333,910 | [Cali*.road-d (864 MB)](/California.road-d.tar.gz) | [Cali*.road-t (845 MB)](/California.road-t.tar.gz) | [Cali*.co (338 MB)](/California.co.tar.gz) |
| Florida | 9,303,268 | 20,249,786 | [Flor*.road-d (493 MB)](/Florida.road-d.tar.gz) | [Flor*.road-t (482 MB)](/Florida.road-t.tar.gz) | [Flor*.co (186 MB)](/Florida.co.tar.gz) |
| Newyork | 6,959,649 | 14,675,944 | [Newy*.road-d (357 MB)](/Newyork.road-d.tar.gz) | [Newy*.road-t (348 MB)](/Newyork.road-t.tar.gz) | [Newy*.co (139 MB)](/Newyork.co.tar.gz) |
| Colorado | 5,118,452 | 10,799,592 | [Colo*.road-d (261 MB)](/Colorado.road-d.tar.gz) | [Colo*.road-t (255 MB)](/Colorado.road-t.tar.gz) | [Colo*.co (107 MB)](/Colorado.co.tar.gz) |


### China (Cities)
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| Chongqing | 1,185,464 | 2,428,866 | [Chon*.road-d (55 MB)](/Chongqing.road-d.tar.gz) | [Chon*.road-t (53 MB)](/Chongqing.road-t.tar.gz) | [Chon*.co (23 MB)](/Chongqing.co.tar.gz) |
| Guangzhou | 490,809 | 1,043,764 | [Guan*.road-d (23 MB)](/Guangzhou.road-d.tar.gz) | [Guan*.road-t (22 MB)](/Guangzhou.road-t.tar.gz) | [Guan*.co (9 MB)](/Guangzhou.co.tar.gz) |
| Beijing | 451,089 | 985,190 | [Beij*.road-d (22 MB)](/Beijing.road-d.tar.gz) | [Beij*.road-t (21 MB)](/Beijing.road-t.tar.gz) | [Beij*.co (9 MB)](/Beijing.co.tar.gz) |
| Chengdu | 423,434 | 913,718 | [Chen*.road-d (20 MB)](/Chengdu.road-d.tar.gz) | [Chen*.road-t (19 MB)](/Chengdu.road-t.tar.gz) | [Chen*.co (8 MB)](/Chengdu.co.tar.gz) |
| Shanghai | 390,171 | 855,982 | [Shan*.road-d (19 MB)](/Shanghai.road-d.tar.gz) | [Shan*.road-t (18 MB)](/Shanghai.road-t.tar.gz) | [Shan*.co (7 MB)](/Shanghai.co.tar.gz) |
| Tianjin | 251,116 | 565,562 | [Tian*.road-d (12 MB)](/Tianjin.road-d.tar.gz) | [Tian*.road-t (12 MB)](/Tianjin.road-t.tar.gz) | [Tian*.co (5 MB)](/Tianjin.co.tar.gz) |
| Shenzhen | 236,647 | 517,110 | [Shen*.road-d (11 MB)](/Shenzhen.road-d.tar.gz) | [Shen*.road-t (10 MB)](/Shenzhen.road-t.tar.gz) | [Shen*.co (4 MB)](/Shenzhen.co.tar.gz) |
| Nanjing | 146,839 | 321,958 | [Nanj*.road-d (6 MB)](/Nanjing.road-d.tar.gz) | [Nanj*.road-t (6 MB)](/Nanjing.road-t.tar.gz) | [Nanj*.co (2 MB)](/Nanjing.co.tar.gz) |
| Xian | 123,995 | 281,542 | [Xian*.road-d (6 MB)](/Xian.road-d.tar.gz) | [Xian*.road-t (5 MB)](/Xian.road-t.tar.gz) | [Xian*.co (2 MB)](/Xian.co.tar.gz) |
| Haikou | 45,948 | 98,566 | [Haik*.road-d (2 MB)](/Haikou.road-d.tar.gz) | [Haik*.road-t (1 MB)](/Haikou.road-t.tar.gz) | [Haik*.co (1 MB)](/Haikou.co.tar.gz) |
| Hongkong | 43,620 | 91,542 | [Hong*.road-d (1 MB)](/Hongkong.road-d.tar.gz) | [Hong*.road-t (1 MB)](/Hongkong.road-t.tar.gz) | [Hong*.co (1 MB)](/Hongkong.co.tar.gz) |

### China (Provinces)


## Urban Logistics
