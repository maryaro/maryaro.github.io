#### Project 2
The purpose of this project is to show a time lapse of the construction of residential buildings in the Mount Winans
neighborhood of Baltimore

#### Data Source
Real Property Dataset from the City of Baltimore Open GIS Data Site

#### Projection
WGS 84/Pseudo-Mercator

#### Neighborhood selection: Mount Winans
  - Located in southwest Baltimore near the construction of the early railroad
  - Has a long history of housing construction

#### Year Classifications:
- 1866-1904: Post Civil War and Great Baltimore Fire, leading to changes in building codes
- 1905-1936: United States Housing Act of 1937 (Wagner-Steagall Bill) - created a
 federally funded housing program
- 1938 - 1978: Federal government banned consumer uses of lead paint in 1978
- 1979 - 2018: Present day

#### Python:
To change the symbology of the real property layer
```python
def change_symbology():
    # Change color of real property layer to tan
    layer = iface.activeLayer()
    renderer = layer.renderer()
    symbol = renderer.symbol()
    symbol.setColor(QColor(254,215,144))
    # Update layer and legend
    layer.triggerRepaint()
    iface.layerTreeView().refreshLayerSymbology(layer.id())
```

To select the neighborhoods:
```Python
from qgis.utils import iface
from PyQt5.QtCore import Qt

# load layer
def load_real_property():
    iface.addVectorLayer('Z:/GES_486/Project_2/data/Real_Property/Real_Property.shp', 'real property', 'ogr')

# select neighborhood, residential buildings, and a year
def attribute_nbhd():
    layer = iface.activeLayer()
    layer.selectByExpression('"NEIGHBOR" = \'MOUNT WINANS\' and "USEGROUP" = \'R\' and "year_build" >= 1803 and "year_build" <= 1860', QgsVectorLayer.SetSelection)
    # update selection to red
    iface.mapCanvas().setSelectionColor(QColor("red"))


load_real_property()
attribute_nbhd()
```
This code was run for each time period to get a new layer.

Additional steps:
- Create layer from the selected features only
- Create centroids
- Create hexagonal grid over study area
- Join attributes by location with centroids and grid as inputs
- 2.5D symbology for hexagons


#### Results:

![gif](http://maryaro.github.io/projec_2/mt_winans.gif "map")
