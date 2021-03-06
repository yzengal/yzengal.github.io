---
layout: archive
title: "Datasets"
permalink: /datasets/
author_profile: true
---

{% include base_path %}
{% include toc %}

In the following, I collect some interesting real-world datasets in spatial databases.

## Road Networks
These real-world road networks were extracted from **OpenStreetMap** on Feb. 2021, based on the processing method in our VLDB'18 paper.
If you want to use the road networks below, please consider citing this homepage and our VLDB'18 paper ([BibTex](https://dblp.uni-trier.de/rec/journals/pvldb/TongZZCYX18.html?view=bibtex)).
Briefly speaking, the datasets are obtained based on the following steps.

1. We download region/country .osm from [Geofabrik](http://download.geofabrik.de/index.html), which maintains the OpenStreetMap data
2. We extract the exact .osm based on the corresponding .poly via [Osmconvert](https://wiki.openstreetmap.org/wiki/Osmconvert)
3. We extract the graph files based from the corresponding .osm via [OsmToRoadGraph](https://github.com/AndGem/OsmToRoadGraph), where network type is car

Notice, in these graphs, the unit of distance is meter and the unit of travel time is second.
If you want to do shortest distance/path queries on these graphs, I think the VLDB'18 paper named "An Experimental Study on Hub Labeling based Shortest Path Algorithms" from Ye Li et al. could be very useful (see their paper for more details).
I have revised their source code to fit the double-type of edge weights (the source code is [here](https://github.com/BUAA-BDA/sspexp_clone)).
 
Large datasets (USA and Chinese provinces) can be downloaded from my [Tencent Cloud](https://share.weiyun.com/70dwzVOX).
 
### USA 
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| California | 16,129,269 | 34,333,910 | [Cali*.road-d (864 MB)](https://github.com/yzengal/RoadNetwork-USA-Part2/blob/main/California.road-d.tar.gz) | [Cali*.road-t (845 MB)](https://github.com/yzengal/RoadNetwork-USA-Part2/blob/main/California.road-t.tar.gz) | [Cali*.co (338 MB)](https://github.com/yzengal/RoadNetwork-USA-Part2/blob/main/California.co.tar.gz) |
| Florida | 9,303,268 | 20,249,786 | [Flor*.road-d (493 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Florida.road-d.tar.gz) | [Flor*.road-t (482 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Florida.road-t.tar.gz) | [Flor*.co (186 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Florida.co.tar.gz) |
| Newyork | 6,959,649 | 14,675,944 | [Newy*.road-d (357 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Newyork.road-d.tar.gz) | [Newy*.road-t (348 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Newyork.road-t.tar.gz) | [Newy*.co (139 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Newyork.co.tar.gz) |
| Colorado | 5,118,452 | 10,799,592 | [Colo*.road-d (261 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Colorado.road-d.tar.gz) | [Colo*.road-t (255 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Colorado.road-t.tar.gz) | [Colo*.co (107 MB)](https://github.com/yzengal/RoadNetwork-USA/blob/main/Colorado.co.tar.gz) |

### China (Cities)
 
| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| Chongqing | 1,185,464 | 2,428,866 | [Chon*.road-d (55 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chongqing.road-d.tar.gz) | [Chon*.road-t (53 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chongqing.road-t.tar.gz) | [Chon*.co (23 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chongqing.co.tar.gz) |
| Guangzhou | 490,809 | 1,043,764 | [Guan*.road-d (23 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Guangzhou.road-d.tar.gz) | [Guan*.road-t (22 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Guangzhou.road-t.tar.gz) | [Guan*.co (9 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Guangzhou.co.tar.gz) |
| Beijing | 451,089 | 985,190 | [Beij*.road-d (22 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Beijing.road-d.tar.gz) | [Beij*.road-t (21 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Beijing.road-t.tar.gz) | [Beij*.co (9 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Beijing.co.tar.gz) |
| Chengdu | 423,434 | 913,718 | [Chen*.road-d (20 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chengdu.road-d.tar.gz) | [Chen*.road-t (19 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chengdu.road-t.tar.gz) | [Chen*.co (8 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Chengdu.co.tar.gz) |
| Shanghai | 390,171 | 855,982 | [Shan*.road-d (19 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shanghai.road-d.tar.gz) | [Shan*.road-t (18 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shanghai.road-t.tar.gz) | [Shan*.co (7 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shanghai.co.tar.gz) |
| Tianjin | 251,116 | 565,562 | [Tian*.road-d (12 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Tianjin.road-d.tar.gz) | [Tian*.road-t (12 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Tianjin.road-t.tar.gz) | [Tian*.co (5 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Tianjin.co.tar.gz) |
| Shenzhen | 236,647 | 517,110 | [Shen*.road-d (11 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shenzhen.road-d.tar.gz) | [Shen*.road-t (10 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shenzhen.road-t.tar.gz) | [Shen*.co (4 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Shenzhen.co.tar.gz) |
| Nanjing | 146,839 | 321,958 | [Nanj*.road-d (6 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Nanjing.road-d.tar.gz) | [Nanj*.road-t (6 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Nanjing.road-t.tar.gz) | [Nanj*.co (2 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Nanjing.co.tar.gz) |
| Xi'an | 123,995 | 281,542 | [Xian*.road-d (6 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Xian.road-d.tar.gz) | [Xian*.road-t (5 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Xian.road-t.tar.gz) | [Xian*.co (2 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Xian.co.tar.gz) |
| Haikou | 45,948 | 98,566 | [Haik*.road-d (2 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Haikou.road-d.tar.gz) | [Haik*.road-t (1 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Haikou.road-t.tar.gz) | [Haik*.co (1 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Haikou.co.tar.gz) |
| Hong Kong | 43,620 | 91,542 | [Hong*.road-d (1 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Hongkong.road-d.tar.gz) | [Hong*.road-t (1 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Hongkong.road-t.tar.gz) | [Hong*.co (1 MB)](https://github.com/yzengal/RoadNetwork-China-City/blob/main/Hongkong.co.tar.gz) |

### China (Provinces)

| Description      | # Vertices | # Edges | Distance graph | Travel time graph | Coordinates |
| --------         | ---------- | ------- | -------------- | ----------------- | ----------- |
| Sichuan | 3,398,810 | 6,960,562 | [Sich*.road-d (168 MB)](https://github.com/yzengal/RoadNetwork-China-Province-Part2/blob/main/Sichuan.road-d.tar.gz) | [Sich*.road-t (162 MB)](https://github.com/yzengal/RoadNetwork-China-Province-Part2/blob/main/Sichuan.road-t.tar.gz) | [Sich*.co (67 MB)](https://github.com/yzengal/RoadNetwork-China-Province-Part2/blob/main/Sichuan.co.tar.gz) |
| Guangdong | 2,898,023 | 6,143,156 | [Guan*.road-d (148 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangdong.road-d.tar.gz) | [Guan*.road-t (142 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangdong.road-t.tar.gz) | [Guan*.co (58 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangdong.co.tar.gz) |
| Hebei | 2,313,690 | 4,976,158 | [Hebe*.road-d (119 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hebei.road-d.tar.gz) | [Hebe*.road-t (115 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hebei.road-t.tar.gz) | [Hebe*.co (46 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hebei.co.tar.gz) |
| Zhejiang | 2,304,979 | 4,853,370 | [Zhej*.road-d (116 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Zhejiang.road-d.tar.gz) | [Zhej*.road-t (111 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Zhejiang.road-t.tar.gz) | [Zhej*.co (46 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Zhejiang.co.tar.gz) |
| Fujian | 1,643,318 | 3,391,506 | [Fuji*.road-d (79 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Fujian.road-d.tar.gz) | [Fuji*.road-t (76 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Fujian.road-t.tar.gz) | [Fuji*.co (32 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Fujian.co.tar.gz) |
| Hunan | 1,620,794 | 3,331,150 | [Huna*.road-d (78 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hunan.road-d.tar.gz) | [Huna*.road-t (75 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hunan.road-t.tar.gz) | [Huna*.co (32 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hunan.co.tar.gz) |
| Jiangsu | 1,506,773 | 3,326,132 | [Jian*.road-d (78 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangsu.road-d.tar.gz) | [Jian*.road-t (75 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangsu.road-t.tar.gz) | [Jian*.co (30 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangsu.co.tar.gz) |
| Guangxi | 1,473,382 | 3,022,138 | [Guan*.road-d (70 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangxi.road-d.tar.gz) | [Guan*.road-t (67 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangxi.road-t.tar.gz) | [Guan*.co (29 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Guangxi.co.tar.gz) |
| Henan | 1,410,007 | 3,062,214 | [Hena*.road-d (71 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Henan.road-d.tar.gz) | [Hena*.road-t (69 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Henan.road-t.tar.gz) | [Hena*.co (28 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Henan.co.tar.gz) |
| Jiangxi | 1,275,488 | 2,635,798 | [Jian*.road-d (61 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangxi.road-d.tar.gz) | [Jian*.road-t (58 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangxi.road-t.tar.gz) | [Jian*.co (25 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jiangxi.co.tar.gz) |
| Shandong | 1,230,449 | 2,769,058 | [Shan*.road-d (64 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shandong.road-d.tar.gz) | [Shan*.road-t (62 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shandong.road-t.tar.gz) | [Shan*.co (24 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shandong.co.tar.gz) |
| Inner Mongolia | 1,131,527 | 2,394,764 | [Inne*.road-d (55 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/InnerMongolia.road-d.tar.gz) | [Inne*.road-t (53 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/InnerMongolia.road-t.tar.gz) | [Inne*.co (22 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/InnerMongolia.co.tar.gz) |
| Hubei | 1,057,791 | 2,202,816 | [Hube*.road-d (50 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hubei.road-d.tar.gz) | [Hube*.road-t (48 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hubei.road-t.tar.gz) | [Hube*.co (21 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hubei.co.tar.gz) |
| Shanxi | 980,205 | 2,044,104 | [Shan*.road-d (46 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shanxi.road-d.tar.gz) | [Shan*.road-t (44 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shanxi.road-t.tar.gz) | [Shan*.co (19 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Shanxi.co.tar.gz) |
| Anhui | 966,953 | 2,063,316 | [Anhu*.road-d (47 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Anhui.road-d.tar.gz) | [Anhu*.road-t (45 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Anhui.road-t.tar.gz) | [Anhu*.co (19 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Anhui.co.tar.gz) |
| Jilin | 640,815 | 1,348,070 | [Jili*.road-d (30 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jilin.road-d.tar.gz) | [Jili*.road-t (29 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jilin.road-t.tar.gz) | [Jili*.co (12 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Jilin.co.tar.gz) |
| Liaoning | 633,561 | 1,340,996 | [Liao*.road-d (30 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Liaoning.road-d.tar.gz) | [Liao*.road-t (29 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Liaoning.road-t.tar.gz) | [Liao*.co (12 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Liaoning.co.tar.gz) |
| Heilongjiang | 629,148 | 1,361,172 | [Heil*.road-d (31 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Heilongjiang.road-d.tar.gz) | [Heil*.road-t (29 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Heilongjiang.road-t.tar.gz) | [Heil*.co (12 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Heilongjiang.co.tar.gz) |
| Hainan | 311,583 | 648,558 | [Hain*.road-d (14 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hainan.road-d.tar.gz) | [Hain*.road-t (13 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hainan.road-t.tar.gz) | [Hain*.co (6 MB)](https://github.com/yzengal/RoadNetwork-China-Province/blob/main/Hainan.co.tar.gz) |


## Urban Logistics

These datasets are under maintainence.
