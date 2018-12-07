## GES 486

#### Project 1
The purpose of this project is to show the average year built of residential housing in 4 Baltimore
neighborhoods based on historical events such as the construction of the B&O railroad and ban on lead paint

#### Data Source
Real Property Dataset from the City of Baltimore Open GIS Data Site

#### Projection
WGS 84/Pseudo-Mercator

#### Neighborhood selection:
  - Mount Vernon: Historic neighborhood
  - Heritage Crossing: Home to McCulloh homes, one of the city's first federally funded housing programs
  - Woodbourne-Heights: Designated one of Baltimore's
  "most improved" neighborhoods in a
   [2016 Baltimore Sun Article](http://www.baltimoresun.com/business/real-estate/bs-re-hot-city-neighborhoods-20170216-story.html)
  - Mount Winans: Located in southwest Baltimore near the construction of the early railroad

#### Year Built Classifications:
- 1803: First recorded residential buildings in dataset
- 1830: Baltimore Ohio railroad - first intercity railroad,
operated until 1987 - connected Ellicott Mills to west Baltimore
- 1861-1865: Civil War - raids on railroad
- 1904: Great Baltimore Fire, leading to changes in building codes
- 1937: United States Housing Act of 1937 (Wagner-Steagall Bill) -
 federally funded housing program, including McCulloh homes
- 1968: Fair Housing Act (April 11, 1968) signed days after race riots
- 1978: Federal government banned consumer uses of lead paint
- 2018: Present day - through the 1990s, not much of the housing segregation has changed,
with most federally funded housing still located in the city

#### Procedures and Tools Used:
- Real Property Dataset converted to a SpatialLite database
- SQL query to create `year_classify` on a scale of 1-9 (assigning `NULL` to 0)

![query](https://maryaro.github.io/query_sc.PNG "Query")
- Convert `year_classify` to `int` instead of `string`
- Create centroids for the selected neighborhoods
- Create hexagonal grid over study area
- Join attributes by location (summary) with centroids and grid as inputs
and mean of `year_classify` calculated
- Graduated classification divided by 1, 2, 3, etc. and shown with a color ramp
##### 3D Map:
  - 2.5D map and graduated classification

#### Results:
![Map](https://project_1/map_sc_final.PNG "Map")

![3d](https://project_1/3d_sc.PNG "3D Map")

