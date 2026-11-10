# kampala-cbd-fire-map

Static GitHub Pages site for an interactive fire-safety map of Kampala's central business district. Live at https://gavacharles.github.io/kampala-cbd-fire-map/

Map and analysis by Gava Charles.

## Contents

| File | What it is |
|---|---|
| `index.html` | The map application (2D/3D map, layers, search, building details, showcase view) |
| `data.json` | Building, road and layer data loaded by the page |
| `satellite.webp` | Satellite image overlay |
| `.nojekyll` | Serve files as they are on GitHub Pages |

The files are exported from the analysis repository (`scripts/viz/05_export_web.py` in kampala-cbd-fire-safety); edit there, re-export, then commit and push here.

## Layers

Fire path, fire-spread groups, hose reach, response time, building height, spacing, surface heat, urban fabric, new buildings since 2016, appliance routes and block priority, plus overlays for documented fires and a Sentinel-2 image. A fixed-size showcase view for stills and video is available at `#v=show&w=1080&h=1080&b=-20` (`b` sets the bearing).

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Data sources

Overture Maps (OpenStreetMap, Google Open Buildings, Microsoft) for buildings and places; OpenStreetMap contributors (ODbL) for roads, features and names; Google Open Buildings 2.5D Temporal for heights; Landsat 8/9 for surface temperature; Sentinel-2 imagery; press reports for documented fires. Desk study on open data; screening only, not an assessment of any individual building.
