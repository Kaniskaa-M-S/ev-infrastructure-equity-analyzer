# EV Infrastructure Equity Analyzer

An interactive Streamlit web application for analyzing zero-emission vehicle (ZEV) 
infrastructure equity, corridor coverage gaps, and charging station suitability 
across New York State. Built for transportation planners and policymakers.

## Screenshots

### Landing Page
![Landing Page](screenshots/01_landing_page.png)

### Station Placement Priority Analysis
![Priority Zones Map](screenshots/02_priority_zones_map.png)

### Corridor Spacing Analysis
![Corridor Spacing](screenshots/03_corridor_spacing_map.png)

### Optimization Parameters
![Optimization Parameters](screenshots/04_optimization_parameters.png)

## Features

- **Equity Coverage Index** — identifies underserved communities and DAC zones 
  lacking adequate EV charging access
- **Queue Risk Analysis** — flags high-demand stations at risk of congestion 
  based on EV registration density
- **Corridor Spacing Analysis** — evaluates charging coverage along NYS highway 
  corridors with gap categorization (Well Covered / Adequate / Moderate Gap / Critical Gap)
- **Station Placement Priority** — multi-criteria optimization scoring 934 priority 
  zones across NYS with adjustable weights for corridor gap, equity, queue risk, 
  and low-density factors
- **Interactive Maps** — real-time filtering, sliders, and toggles built with 
  Folium and Leaflet

## Tech Stack

Python · Streamlit · GeoPandas · Folium · Pandas · NumPy · Shapely

## Data Sources

All data used is publicly available:
- NYSERDA Disadvantaged Communities Shapefile
- Alternative Fuels Corridors (FHWA / AltFuels)
- NY EV Charging Stations (AFDC / DOE)
- NY EV Registrations (NYS DMV)
- Census Tract Boundaries (US Census Bureau)
- NYS Civil Boundaries

## Running Locally

This tool requires geospatial datasets (EV stations, census tracts, corridor 
shapefiles) that are publicly available from the sources listed above. Download 
and place them in the `Spatial/Data/` and `Spatial/GEOJSON/` directories, 
then run:
```bash
pip install -r requirements.txt
streamlit run app.py
```

Data loading scripts are provided in `convert_geopandas.py` to preprocess 
raw shapefiles into the required GeoJSON format.

## Presentations & Recognition

**Smart Mapping in Action: GIS Applications in Housing, AEC, and the Transition to Zero-Emission Vehicles**  
American Planning Association — New York Upstate Chapter Annual Conference, October 2025

Presented alongside senior planners from LaBella Associates, exploring how GIS technologies 
and data-driven tools enable smarter, more sustainable planning decisions.

- [LaBella Associates Conference Post →](https://labellapc.com/news/labella-presenting-at-the-apa-new-york-upstate-chapters-2025-annual-conference/)
- [Official Speaker Bios (APA NY Upstate 2025) →](https://static1.squarespace.com/static/5717ac15a3360cf4481e28bc/t/68ddadd878a0ad68d3177dd1/1759358424566/NY+Upstate+APA+2025+Conference+Speaker+Bios.pdf)
