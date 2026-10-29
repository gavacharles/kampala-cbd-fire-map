# Kampala CBD Fire Map

Interactive map of fire safety conditions in Kampala's central business district: 11,107 buildings within 1.5 km of Kampala Road.

**Map and analysis by Gava Charles.**

**Live page:** https://gavacharles.github.io/kampala-cbd-fire-map/

## Layers

- **Fire-spread groups:** buildings linked by gaps narrower than a chosen threshold (0–10 m).
- **Hose reach:** buildings extending more than 45 m from a road a fire appliance can use.
- **Response time:** drive time from Kampala Fire Station at different traffic speeds, with an optional modelled second station.
- **Height:** satellite-estimated building heights; switch to 3D to see them extruded.
- **Spacing:** gap from each building to its nearest neighbour.
- **Surface heat:** relative dry-season land-surface temperature.
- **Block priority:** equal-weight combination of group size, hose reach, congested drive time and surface heat per 100 m block.

## Data and caveats

Desk study on open data; no field survey.

- Buildings: Overture Maps 2026-10-21 (OpenStreetMap, Google Open Buildings, Microsoft). Footprints are accurate to about 1–3 m.
- Roads, features and building names: © OpenStreetMap contributors, ODbL. Places inside buildings: Overture Maps places.
- Heights: Google Open Buildings 2.5D Temporal (2023), calibrated on 50 OSM-tagged buildings; right height band for 56%, within one band for 88%.
- Drive times use assumed speeds by road class and exclude call handling and turnout.
- Surface heat: Landsat 8/9 band 10 without atmospheric correction; relative values only.

## Using the map

- **Rotate:** the ↺ N ↻ buttons, right-drag, Ctrl-drag or a two-finger twist. Works in 2D and 3D; 3D also tilts.
- **Hover** a building to see its name and the places inside it, where mapped (OpenStreetMap and Overture places).
- **Tap** a building for full details.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
