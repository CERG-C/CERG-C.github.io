# Gentle introduction to QGIS 

*Geographic Information Systems* – or **GIS** – are tools designed for capturing, storing, checking, and displaying data related to positions on Earth’s surface - or *spatial* data. This is a broad topic, too broad to be entirely covered here, and some of you might already be familiar with it. For the others, we will try to keep the information to a minimum required for the exercise. Bear in mind that the main use for GIS here will be restricted to *visualisation* (rather than analyses) of geospatial data. 

For more information, you can visit these links:

- [QGIS](https://docs.qgis.org/3.22/en/docs/gentle_gis_introduction/introducing_gis.html)
- [Wikipedia](https://en.wikipedia.org/wiki/Geographic_information_system)
- [National Geographic](https://www.nationalgeographic.org/encyclopedia/geographic-information-system-gis/)
- [ESRI](https://www.esri.com/en-us/what-is-gis/overview)

GIS are extensively used in the study of natural hazards and their risks as they allow to analyse the spatial relationship between hazardous phenomena and exposed elements. The objectives of this short introduction are to provide you with the basic GIS knowledge necessary to fully understand the volcanic hazard assessment of the following classes. Specifically, the objectives are:

1. Getting to know the QGIS interface
2. Load data into QGIS
3. Creating and saving maps

## Some basic GIS concepts

The most common GIS most of us use on a daily basis is [OpenStreetMap](https://www.openstreetmap.org) (*OSM* for short) or any equivalent. There, a lot of data is stored and *georeferenced*, meaning that all piece of data has a geospatial reference and is able to be located on the globe's surface. In GIS, datasets are stored in two main forms: **vector** and **raster**. Think of it as the same fundamental difference that exists between *Illustrator* and *Photoshop*.

### Vector data 

[OSM](https://www.openstreetmap.org) contains only *vector* data, which can be either *points*, *lines* (e.g., roads) or *polygons* (e.g., lakes). For points, a vector GIS data showing some information about some of my favourite Swiss mountains could look like this:

| Latitude | Longitude | Name         | Altitude | Canton | First ascent |
|:---------|:----------|:-------------|:---------|:-------|:-------------|
| 45.976   | 7.658     | Matterhorn   | 4,478 m  | Valais | 1865         |
| 46.034   | 7.612     | Dent Blanche | 4,357 m  | Valais | 1862         |

In this case, the `Latitude` and `Longitude` columns hold *geographical* data, whereas the other columns hold *non-geographical* attributes. More information is available on the [Wikipedia](https://en.wikipedia.org/wiki/GIS_file_formats#Raster) and [QGIS](https://docs.qgis.org/3.22/en/docs/gentle_gis_introduction/raster_data.html) websites.

!!! info "Coordinate systems"

    In the example above, we used `Latitude` and `Longitude` to express the `y` and `x` coordinates of the points. This seems trivial, but actually opens a complex problem which is *how to represent a [distorted spherical body](https://www.esa.int/ESA_Multimedia/Images/2010/04/Earth_Explorers_The_Earth_s_true_shape)* onto a flat map. This has been a problem since about [650 BCE](https://www.worldatlas.com/articles/the-oldest-map-projections-in-the-world.html), and [a lot of different projections](https://bl.ocks.org/mbostock/raw/3711652/?raw=true) have been proposed, each with benefits and negative aspects. In any case, in the classes we might refer to either *coordinate systems* or *EPSG* (an [international code](https://epsg.io) referencing the various projections). More information is available [here](https://docs.qgis.org/3.22/en/docs/gentle_gis_introduction/coordinate_reference_systems.html). 

### Raster data

Raster data are stored as a grid of values - or *pixels.* There is no raster data on [OSM](https://www.openstreetmap.org), but two common raster datasets are *satellite imagery* or *digital elevation models* (or DEM). The main difference with vector datasets is that if you zoom sufficiently, *pixels* will start to appear. The zoom level at which this effect occurs depends on the raster's *resolution*, i.e., the size of a given pixel in the `x` and `y` directions. More information is available on the [QGIS](https://docs.qgis.org/3.22/en/docs/gentle_gis_introduction/vector_data.html) website.

## QGIS 

*Quantum GIS* – or QGIS – is an open-source GIS software. We use it as it is free, cross-platform and powerful. A comprehensive documentation on [QGIS](https://docs.qgis.org/3.22/en/docs/user_manual/index.html) (and [GIS in general](https://docs.qgis.org/3.22/en/docs/gentle_gis_introduction/index.html)) is available on the QGIS website.

### The QGIS interface 

The QGIS interface is shown in Figure 1. Note that the Graphical User Interface (GUI) is highly customisable and might look different at first, but the red numbers indicate the main common components. 

<figure markdown>
  ![QGIS_interface](img/qgis/qgis_interface.png)
  <figcaption>Figure 1: The QGIS interface</figcaption>
</figure>

The main component of the interface are:

1. [Menu bar](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#label-menubar)
2. [Toolbars](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#sec-panels-and-toolbars)
3. [Panels](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#sec-panels-and-toolbars)
4. [Map view](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#label-mapview)
5. [Status bar](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#label-statusbar)

Let's focus on specific aspects of the GUI. 

#### Panels

Panels are special widgets that you can interact with, and QGIS provides [multiple panels](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/qgis_gui.html#panels) for various tasks. Here, let's focus on the [Layer panel](https://docs.qgis.org/3.22/en/docs/user_manual/introduction/general_tools.html#label-legend). 