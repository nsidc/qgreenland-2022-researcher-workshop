---
title: "Analyze your dataset"
index: 210
---

## 📈 Create an analysis narrative

Using a combination of Markdown and code cells in your notebook from the previous
exercise, perform your analysis if possible. If your analysis is not possible at the
current time, document why this is the case and jump to the fallback activity.


## 📝 Add a summary

In a final section of your notebook:

* Tell us about what you learned.
* Provide a brief overview of your analysis / ideas for future analysis with
  the dataset you chose.


## 🧠 Fallback activity: Make your dataset "QGreenland-friendly"

If the analysis is not currently possible, explain why this is the case in your
Notebook, and what you would need to make it possible. Then, make your dataset as
friendly as possible to usage with QGreenland:

* Ensure dataset is in EPSG:3413 projection. This minimizes computation required to
  display the dataset by avoiding on-the-fly reprojection to the QGIS viewport's
  projection.
* Use the QGreenland "Greenland-focused boundary" layer to subset/clip the
  data (`Reference/QGreenland boundaries` in the QGreenland **Layers Panel**). This
  optimizes space used on disk by the new layer.
* Make sure the data is GeoTIFF (if raster) or GeoPackage (if vector).
* _TODO: What about overviews, compression? Other?_

Does your dataset display correctly alongside other data in QGreenland after these
changes?


### Analysis practice

_TODO: consider additional data/analysis scenarios that groups can try if they have the
time / do not have an analysis for their dataset._
