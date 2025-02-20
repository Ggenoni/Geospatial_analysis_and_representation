# Bikeability and Walkability Analysis of Trento  

This repository contains geospatial analysis scripts and datasets used to assess the **bikeability** and **walkability** of the city of Trento. The analysis is based on **OpenStreetMap data** and the **Comune di Trento Open Data portal**, utilizing **spatial network analysis** and **urban accessibility metrics**.  

## 📌 Overview  

The project evaluates **cycling and pedestrian infrastructure** in Trento by computing indicators such as:  
- **Bike lane length and coverage**  
- **Bike parking density**  
- **Natural area proportion** along cycling routes  
- **Point of Interest (POI) density** for accessibility  
- **Average slope** of bike lanes  
- **Walkability metrics**, including **intersection density** and **amenity accessibility**  

These indicators are used to construct a **Bikeability Index** and analyze district-level variations in active mobility.  

## 📦 Dependencies  

This project relies on the following Python libraries:  

| Library     | Version |
|------------|---------|
| `geopandas`  | 1.0.1  |
| `pandas`     | 2.2.2  |
| `matplotlib` | 3.10.0 |
| `osmnx`      | 2.0.1  |
| `seaborn`    | 0.13.2 |
| `pandana`    | 0.7    |
| `numpy`      | 1.26.4 |
| `scipy`      | 1.13.1 |
| `networkx`   | 3.4.2  |
| `shapely`    | 2.0.7  |

## 🌍 Data Sources
This project uses geospatial datasets from **Comune di Trento Open Data** and **OpenStreetMap (OSM)**.

### 🏙️ Open Data - Comune di Trento  
Most datasets were sourced from the [Comune di Trento Open Data portal](https://www.comune.trento.it/Aree-tematiche/Open-Data), provided in GeoJSON format.

- **🗺️ Trento Districts (`circoscrizioni`)**  
  Administrative boundaries of Trento’s **12 districts**, used for spatial aggregation.  

- **🚴‍♂️ Bike Lanes (`bike_lanes`)**  
  Contains Trento’s **bike lanes and shared pedestrian-cyclist paths**, classified under municipal or provincial jurisdiction.  

- **🅿️ Bike Parking (`bike_parking`)**  
  Information on **protected long-term bike parking areas**, including capacity and location.  

- **🏔️ Bike Racks (`racks`)**  
  Maps **bike racks** in the limited traffic zone, categorized by type and capacity.  

- **Contour Lines (`elevation`)**  
  **Topographic contour lines** with a 10-meter vertical interval, derived from aerial surveys.  

### 🌐 OpenStreetMap Data  
Additional datasets were extracted using the `osmnx` library.

- **🌳 Natural Areas (`natural_areas`)**  
  Includes **parks and grassy areas**, retrieved by filtering OSM features tagged as `leisure=park` or `landuse=grass`.  

- **📍 Points of Interest (`pois`)**  
  Diverse range of **urban amenities**, including shops, offices, and public services.  

- **🚦 Street Network (`streets`)**  
  The **road network** of Trento, extracted using `network_type="all"`.  

- **🚶‍♂️ Pedestrian Network (`walkways`)**  
  The **walkable network**, including sidewalks, footpaths, and pedestrian streets (`network_type="walk"`).  

Each dataset was reprojected to **EPSG:32632 (WGS 84 / UTM zone 32N)** for spatial analysis.  


