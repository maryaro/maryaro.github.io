## Final Project
### Mary Aronne

#### Purpose
The purpose of this project is to use different QGIS techniques to study elevation and rainfall in New Zealand. New Zealand has an interesting, 
mountainous topography and straddles the Australian and Pacific tectonic plates. The South Island has the Southern Alps, and the 
North Island is less mountainous but has some volcanoes. This project uses a 3D map to see elevation, a hexagonal map to better visualize average yearly
rainfall, and a statistical analysis of elevation and rainfall in GeoDa.

This project is slightly adapted from the original proposal, as it was dependent on the results of the GES 381: remote sensing project I did,
which had interesting but unexpected results, and this new focus is more promising for the purposes of GES 486 and using QGIS.

#### Hexagonal Rainfall Map:
![hex map](https://maryaro.github.io/final_project/rain_map.png "Hex Map")

- Data source: New Zealand Ministry for the Environment and Environmental Planning

- In QGIS, A hex grid was created over the extent of the layer, and a join attributes by location was used to add rainfall (and elevation, for the 
GeoDa analysis). The symbology was changed to a gradient that showed the rainfall amounts.

- This rainfall map shows more rainfall on the North Island than the South Island, and on the South Island there is more rainfall
in the far south than the northern part of the island.

#### 3D Elevation Map:

![3d 2](https://maryaro.github.io/final_project/3d_zoom_2.PNG "3d 2")
![3d 1](https://maryaro.github.io/final_project/3d_zoom_1.PNG "3d 1")

- The first 3D map focuses the North Island, which you can see has lower elevations than the South Island. There is only one peak that 
sticks out in the center, which is the Ruapehu volcano, which recently erupted in 1996.

- The first 3D map shows a view of the South Island, which prominently features the Southern Alps. The highest peak is Aoraki/Mount Cook
at 3,724 meters. It can be seen as the bright yellow peak near the center and to the west. It is surrounded by many other high peaks.

#### GeoDa Statistical Analysis:

![significance](https://maryaro.github.io/final_project/significance.png "significance")
![cluster](https://maryaro.github.io/final_project/cluster.png "cluster")
![scatter](https://maryaro.github.io/final_project/scatter.png "scatter")
