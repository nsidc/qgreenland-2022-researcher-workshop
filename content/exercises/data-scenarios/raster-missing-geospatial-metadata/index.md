---
title: "Data Scenario: Raster missing geospatial metadata"
categories: ["Data issue"]
listing:
  id: "file-listing"
  type: "table"
  sort-ui: false
  filter-ui: false
  contents:
    - "*"
    - "solutions/*"
---

::: {#file-listing}
:::

::: {.callout-note}
The included data file sample is not a real example of data from NSIDC; it's been
modified from the original ([here](https://nsidc.org/data/nsidc-0092/versions/1)) to
present a challenge.
:::

You download a dataset (`dem_without_metadata.tif`, found in this directory) which
doesn't load as expected in QGIS. When loaded alongside QGreenland, instead of
overlaying the DEM on Greenland, it can be found near the North pole using the "Zoom to
Layer" feature.

![`dem_without_metadata.tif` displayed along with QGreenland](/_media/qgreenland_missing_metadata.png)

The landing page from which you downloaded this DEM states the dataset's [proj4
string](https://proj.org/usage/) is:

```text
+proj=stere +lat_0=90 +lat_ts=71 +lon_0=-39 +x_0=0 +y_0=0 +a=6378137 +rf=298.257024882273 +units=m +no_defs
```

<!-- TODO:
Consider if we should use a named datum in proj4 string instead of +a, +rf params
-->

And the corner coordinates are:

```text
Upper Left  ( -802500.000, -597500.000)
Lower Right (  702500.000,-3402500.000)
```

## Validation

The dataset should include all of the metadata necessary to correctly position
it alongside other layers in QGreenland.

![Solution displayed along with
QGreenland](/_media/qgreenland_edited_metadata.png)
