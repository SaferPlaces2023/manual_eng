---
cover: ../.gitbook/assets/Asset 10.jpg
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: hero
    mask: none
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# 📔 Digital Twin

To start a new project or service on the Saferplaces platform, it is necessary to generate a Digital Twin of the area of interest.

{% content-ref url="creation-of-digital-twin-and-activation-of-the-service-in-the-area-of-interest/" %}
[creation-of-digital-twin-and-activation-of-the-service-in-the-area-of-interest](creation-of-digital-twin-and-activation-of-the-service-in-the-area-of-interest/)
{% endcontent-ref %}

The Digital Twin consists of the following geospatial data:

<details>

<summary>Digital Terrain Model (DTM) - LIDAR</summary>

The SaferPlaces platform allows users to select various available DTM layers with different spatial resolutions.

During the activation phase, DTM levels are sorted in descending order of resolution.

Users can choose from DTMs ranging from the highest spatial resolution (LIDAR) to regional or national products with lower resolution.

Alternatively, if users have their own DTM data, they can upload it directly using the UPLOAD option to create a Digital Twin.

The platform is optimized for working with high-resolution LIDAR DEM data.

The Global pre-loaded and nationally available DTMs are:

* Copernicus DEM&#x20;
* @@@

<br>

</details>

<details>

<summary>Building Footprint - Vector Shapefile</summary>

The building footprint data is used to calculate the Economic Damage associated with flooding events.

This geospatial layer, in vector shapefile format, is automatically acquired from the [Open Street Map](https://osmbuildings.org/?lat=43.94654\&lon=12.63075\&zoom=16.0\&tilt=30) dataset.\
Alternatively, users can upload specific information directly onto the platform using the UPLOAD option.

</details>

<details>

<summary>Infiltration Rate</summary>

This layer represents the soil's infiltration capacity, linked to land use classification. Specifically, urbanized or industrial land use will have an infiltration rate close to zero, while agricultural or green areas will have a rate close to one.

In creating the Digital Twin, Saferplaces uses the 10 m land use layer provided by ESA ([The European Space Agency (ESA) WorldCover 10 m 2021](https://esa-worldcover.org/)).

If more detailed information is available, users can upload a vector shapefile with land use classes using the UPLOAD function.

\\

</details>

<details>

<summary>Lithology</summary>

The soil lithology, defined by texture classes (Sand, Clay, and Silt), affects the capacity and rate of water infiltration, thus reducing surface run-off and helping to mitigate flooding.

This information is an input for the Green-Ampt infiltration model, implemented in specific tools.

The texture data is integrated into the Saferplaces platform, with global coverage and a spatial resolution of 100 m, and is provided by [OpenLandMap](https://opengeohub.org/about-openlandmap/).

</details>

<details>

<summary>Climatic Data</summary>

During the activation phase of the service, it is possible to automatically acquire climatic data from the datasets available in [Copernicus CDS.](https://cds.climate.copernicus.eu)

</details>

<details>

<summary>Satellite Images</summary>

Satellite data processing functions allow the automatic extraction of flooded areas by analyzing both optical and SAR images from [Copernicus Sentinel](https://dataspace.copernicus.eu/explore-data/data-collections).

</details>

{% hint style="danger" %}
For the creation of the new project and the Digital Twin, the essential input data include the DTM and the building "Footprint."

The DTM is the primary and crucial input required by the SaferPlaces flood hazard models.

The activation wizard requires the user to choose from the available data or upload their own for:

* DTM
* BUILDINGS
* INFILTRATION
* LITHOLOGY

Climate data and satellite images are uploaded in the background during the project activation.
{% endhint %}

