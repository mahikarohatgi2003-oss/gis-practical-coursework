# Remote Sensing & GIS — Practical Coursework

QGIS practical file from my B.A. (Hons) Geography degree at Kalindi College, University of Delhi (Remote Sensing and GIS Practical, Unique Paper Code 12291502, 2023–24). This documents hands-on GIS workflows completed end-to-end in QGIS 3.26, from raw aerial photograph interpretation through raster-based vegetation and water indices.

**Author:** Mahika Rohatgi ([LinkedIn](https://linkedin.com/in/mahika-rohatgi) · [GitHub](https://github.com/mahikarohatgi))

## What's in here

The full practical file (with all screenshots and worked examples) is in [`Remote_Sensing_GIS_Practical_File.pdf`](./Remote_Sensing_GIS_Practical_File.pdf). A quick-reference summary of the techniques is below and in [`docs/skills-reference.md`](./docs/skills-reference.md).

## Skills demonstrated

| Area | Techniques |
|---|---|
| **Aerial photo interpretation** | Photo scale computation (focal length/altitude, ground measurement ratio, variable terrain), annotation, image interpretation elements (shape, size, pattern, tone, shadow, association) |
| **Satellite imagery interpretation** | LULC classification from Landsat FCC, spatial resolution concepts |
| **Georeferencing** | GCP-based raster georeferencing (Georeferencer/GDAL plugin), rubber-sheeting for maps without known coordinates |
| **Digitization** | Point/line/polygon vector creation, split-feature tool, error correction (dangles, overshoots, slivers), map layout & export |
| **Attribute & tabular data** | Non-spatial data joins (census data to administrative boundaries), attribute table management |
| **Thematic mapping** | Choropleth maps (graduated symbology), pie charts, histograms |
| **Spatial SQL / queries** | Select by polygon, freehand, radius, value, and expression (LIKE, ILIKE, AND/OR operators) |
| **Geoprocessing** | Buffer, clip, convex hull, dissolve, difference, union |
| **Raster analysis** | NDVI and NDWI computation via Raster Calculator, band math, color ramp symbology |

## Tools

QGIS 3.26 (Georeferencer/GDAL, Raster Calculator, Print Layout), Landsat 8/9 OLI imagery, USGS Earth Explorer, Census of India (2011) district-level data.

## Note

This is coursework, not a research publication — it documents applied GIS competency (software workflows, not novel analysis). For my research work, see the coastal change detection study (DSAS/Landsat, Mirya Bay) and the REE prospectivity mapping project in my other repos.
