# Mekong Mine Detection Pilot

Static site. No build step and no server-side code.

## Deploy

- **GitHub Pages:** push this folder to a repository, then Settings > Pages > Deploy from a branch > `main` / root.
- **Netlify or Cloudflare Pages:** drag this folder onto the dashboard, or connect the repository with an empty build command and `/` as the publish directory.
- **Any web server:** copy the folder as-is.

## Run locally

    python3 -m http.server 8000

Then open http://localhost:8000. Opening `index.html` directly from disk does not work, because the page loads its data with `fetch`.

## Contents

- `index.html` - the app
- `data/app.json` - Stimson mine points, rivers, boundaries, model metrics
- `data/patches.json` - predicted mine footprints, 2025 (GeoJSON)
- `img/` - Sentinel-2 quicklooks, Jan-Mar 2025, one per 10 km block
- `vendor/` - Leaflet 1.9.4, Chart.js 4.4.1
- `assets/` - Thammasat University emblem

Basemap tiles (OpenStreetMap, Esri World Imagery) and fonts (Google Fonts) load from the internet.

## Data credits

Mines and rivers: Stimson Center. Embeddings: The AlphaEarth Foundations Satellite Embedding dataset is produced by Google and Google DeepMind. Land cover: ESA WorldCover 2021. Imagery: Copernicus Sentinel-2. Boundaries: Natural Earth.
