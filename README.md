# Project Heatmap: Community-Level Heat Vulnerability Mapping

# Community-Level Heat Vulnerability Mapping — Kaduna, Nigeria

## Overview
This project develops a **Heat Vulnerability Index (HVI)** for **Kaduna City, Nigeria**, integrating geospatial temperature data with demographic and infrastructural indicators. The goal is to identify urban neighborhoods most at risk from extreme heat exposure and limited adaptive capacity. The work is part of a broader effort to understand climate-related security risks and inform resilience planning across Northern Nigeria.

## Objective
To map and quantify neighborhood-level heat vulnerability by combining:
- **Exposure:** Land Surface Temperature (MODIS or ERA5-Land)
- **Sensitivity:** Population density and demographic composition (WorldPop, GHS-POP)
- **Adaptive Capacity:** Access to cooling infrastructure and socioeconomic proxies (OSM facilities, VIIRS night-time lights)

The resulting Heat Vulnerability Index (HVI) is defined as:
> HVI = α * Exposure + β * Sensitivity - γ * Adaptive Capacity  
> where α=0.45, β=0.35, γ=0.20 (modifiable weights)

## Area of Interest (AOI)
**Kaduna City, Kaduna State, Nigeria**  
Approximate coordinates: *Latitude 10.52° N, Longitude 7.44° E*  
This AOI was selected due to its climatic variability, urban density, and strategic relevance to humanitarian and defense operations in Northern Nigeria.

## Methods
1. **Data Acquisition:** MODIS LST, WorldPop, OSM infrastructure, VIIRS nightlights.  
2. **Processing:** Normalization, raster resampling (100 m resolution), and index computation in Python (`GeoPandas`, `rioxarray`) and Google Earth Engine.  
3. **Analysis:** Aggregation of pixel-level HVI to neighborhood units, ranking of high-risk zones, and validation against known urban heat island patterns.  
4. **Visualization:** Static maps (QGIS) and interactive dashboards (Folium/Plotly).  

## Deliverables
- `hvi_raster.tif` — Heat Vulnerability raster for Kaduna.  
- `neighborhood_hvi.csv` — Mean HVI by neighborhood.  
- `interactive_map.html` — Layered map showing exposure, sensitivity, and adaptive capacity.  
- `community_brief.pdf` — 1-page summary with actionable interventions.  

## Defense and Humanitarian Relevance
Kaduna’s growing exposure to extreme heat has implications for **troop welfare**, **critical infrastructure resilience**, and **civil–military coordination** during climate-induced stress events. This project aims to support operational planning and local adaptation strategies through geospatial evidence.

## Author
**Favour Adebayo**  
Data Analyst & Defence Researcher
