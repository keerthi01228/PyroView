# PyroView 🛰️ — Wildfire Severity & Terrain Risk Explorer

PyroView is a browser-based geospatial visualization project for exploring satellite imagery before and after a wildfire and examining the surrounding terrain.

The project focuses on the Dixie Fire region of California in 2021. It combines pre-fire satellite imagery, a post-fire Normalized Burn Ratio (NBR) visualization, and interactive terrain exploration in a single map interface.

🌐 **Live Website:** [Explore PyroView](https://keerthi01228.github.io/PyroView/)

> **Important:** PyroView is an exploratory visualization tool, not an official wildfire severity classification system or an emergency-warning service.
## 🗺️ Interactive Map

**[Open PyroView Interactive Map](http://127.0.0.1:5500/map.html)**

Explore the pre-fire and post-fire imagery using the interactive swipe comparison and terrain controls.

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

## Architecture and Technology

- **Frontend:** HTML, CSS, and JavaScript
- **Website hosting:** GitHub Pages
- **Interactive mapping:** MapLibre GL JS
- **Swipe comparison:** MapLibre GL Compare
- **Basemap:** OpenFreeMap
- **Satellite imagery:** Pre-fire RGB and post-fire NBR image overlays hosted in Amazon S3
- **Terrain visualization:** Terrarium-encoded elevation tiles

The browser loads the website and retrieves the map styles, imagery, and terrain resources required to display the interactive visualization.

## Data Sources and Attribution

### Satellite Imagery

The project uses pre-fire RGB imagery and a post-fire NBR visualization for the Dixie Fire region.

- **Pre-fire scene date:** July 8, 2021
- **Post-fire scene date:** August 27, 2021
- **Source:** Sentinel-2-derived imagery

Specific scene identifiers, processing details, and complete imagery attribution should be documented when available.

### Terrain Elevation

Terrain visualization uses Terrarium-encoded elevation tiles hosted in the AWS `elevation-tiles-prod` S3 bucket.

- **Dataset information:** [AWS Open Data Registry — Terrain Tiles](https://registry.opendata.aws/terrain-tiles/)
- **Data documentation and attribution:** [Terrain Tiles documentation](https://github.com/tilezen/joerd/tree/master/docs)
- **Attribution guidance:** [Terrain Tiles attribution requirements](https://github.com/tilezen/joerd/blob/master/docs/attribution.md)

The Terrain Tiles dataset combines elevation data from underlying sources. Please consult its attribution guidance for the applicable credits.

### Map Services

- **Basemap:** [OpenFreeMap](https://openfreemap.org/)
- **Map rendering:** [MapLibre GL JS](https://maplibre.org/)

Please consult the relevant service documentation for attribution requirements and usage terms.

## Run Locally

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code.
3. Start the page using the Live Server extension.
4. Open the local URL provided by Live Server in your browser.

An internet connection is required to load the externally hosted map styles, map libraries, imagery, and terrain resources.

## Screenshots

Screenshots can be added here to demonstrate the application's interface and functionality.

Recommended screenshots:

- PyroView landing page.
- Interactive map showing the pre-fire and post-fire comparison.
- Interactive terrain visualization.

## Limitations

- The imagery is provided for visualization and exploration.
- A single-date NBR image alone does not establish official burn severity.
- The application is not intended for emergency response or operational risk decisions.
- The displayed map depends on the availability of external tile, map, and imagery services.
- The availability of the live website depends on the hosting service.

## Project Status

- Landing page published using GitHub Pages.
- Interactive map and its core comparison and terrain controls implemented.
- Satellite imagery hosted in Amazon S3.
- Public website URL available for accessing the project.

The landing page and interactive map navigation should be tested together to confirm that all website features work correctly in the published version.

## License

A license has not yet been specified. See this repository for licensing information once a license file is added.
