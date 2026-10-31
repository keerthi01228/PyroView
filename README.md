# PyroView 🛰️ — Wildfire Severity & Terrain Risk Explorer

PyroView is a browser-based geospatial visualization project for exploring satellite imagery before and after a wildfire and examining the surrounding terrain.

The project focuses on the Dixie Fire region of California in 2021. It combines pre-fire satellite imagery, a post-fire Normalized Burn Ratio (NBR) visualization, and interactive terrain exploration in a single map interface.

> **Important:** PyroView is an exploratory visualization tool, not an official wildfire severity classification system or an emergency-warning service.

## Features

- **Before-and-after comparison:** Use a swipe control to compare pre-fire and post-fire imagery.
- **Satellite imagery visualization:** Explore a pre-fire Sentinel-2 RGB image and a post-fire NBR image.
- **Interactive terrain:** Toggle terrain visualization and adjust terrain exaggeration.
- **Map navigation:** Zoom and pan to explore the mapped area.
- **NBR legend:** View the displayed NBR value range alongside the post-fire visualization.

## Study Area and Imagery

- **Study area:** Dixie Fire region, California, USA
- **Pre-fire scene:** Sentinel-2, July 8, 2021
- **Post-fire scene:** Sentinel-2, August 27, 2021
- **Pre-fire visualization:** RGB satellite imagery
- **Post-fire visualization:** Normalized Burn Ratio (NBR)

NBR is calculated from near-infrared (NIR) and shortwave-infrared (SWIR) reflectance:

`NBR = (NIR - SWIR) / (NIR + SWIR)`

The current post-fire layer displays a single-date NBR image. It does **not** represent differenced NBR (dNBR), and its colors should not be interpreted as verified or official burn-severity categories.

## Technology

- HTML, CSS, and JavaScript
- MapLibre GL JS
- MapLibre GL Compare
- OpenFreeMap basemap
- Terrarium elevation tiles for terrain visualization
- Sentinel-2-derived image overlays

## Run Locally

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code.
3. Start the page using the Live Server extension.
4. Open the local URL provided by Live Server in your browser.

An internet connection is required to load the externally hosted map styles, map libraries, and terrain resources.

## Limitations

- The imagery is provided for visualization and exploration.
- A single-date NBR image alone does not establish official burn severity.
- The application is not intended for emergency response or operational risk decisions.
- The displayed map depends on the availability of external tile and map services.

## Project Status

The interactive map and its core comparison and terrain controls have been implemented. Further work may include improving data documentation, validating imagery and masking, refining the legend, and publishing a hosted version.

## License

A license has not yet been specified. See this repository for licensing information once a license file is added.
