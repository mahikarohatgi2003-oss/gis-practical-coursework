# Quick Reference: Formulas & Workflows

Condensed reference extracted from the full practical file — useful for quick recall in interviews or when reusing these workflows.

## Photo scale formulas

- **Flat terrain, focal length & altitude known:** `S = f / H`
- **Ground measurement:** `S = ab / AB` (photo distance / actual ground distance)
- **Variable terrain (max/min/avg):** `S = f / (H − h)`
- **Using a reference map:** `Scale = (photo distance / map distance) × map scale`

## Georeferencing (QGIS)

1. Enable Georeferencer GDAL plugin (Plugins → Manage and Install Plugins)
2. Raster → Georeferencing → Open Raster
3. Add ≥4 GCPs (Add Point), enter known X/Y (longitude/latitude)
4. Settings → Transformation Settings → Polynomial 1 (or Linear) → Target CRS EPSG:4326 → Start Georeferencing
5. **Rubber sheeting** (no known coordinates): use "From Map Canvas" against a live basemap (e.g. OpenStreetMap) instead of typing coordinates directly

## Digitization

- New Shapefile Layer → set geometry type (Point/Line/Polygon) + CRS
- Toggle Editing → Add Feature → trace → right-click to close/end → fill attribute dialog
- Split Feature tool for carving sub-boundaries out of a digitized outline
- Common errors to check for: dangles, overshoots, undershoots, knots, loops, switchbacks, slivers

## Spatial SQL (Select by Expression) — useful operators

- `"field" LIKE 'D%'` → starts with D
- `"field" ILIKE '%i'` → ends with i (case-insensitive)
- `"field" ILIKE '_O%'` → second character is O
- `"field" % '2'` → modulo (e.g. odd/even values)
- Combine conditions with `AND` / `OR`

## Geoprocessing tools (Vector → Geoprocessing Tools)

| Tool | Function |
|---|---|
| Buffer | Zone of fixed distance around a feature |
| Clip | Keep only input features that fall inside an overlay polygon |
| Convex Hull | Minimum bounding polygon around a feature set |
| Dissolve | Merge features sharing an attribute value, erasing shared boundaries |
| Difference | Keep parts of input layer that fall *outside* an overlay layer |
| Union | Combine two layers, splitting features at their overlaps |

## Raster indices

- **NDVI** (vegetation): `(NIR − Red) / (NIR + Red)`
- **NDWI** (surface water): `(Green − NIR) / (Green + NIR)`

Workflow: Raster → Raster Calculator → build expression from band layers → apply pseudocolor ramp in Layer Properties → Symbology.
