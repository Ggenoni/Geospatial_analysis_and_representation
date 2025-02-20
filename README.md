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

## Data Sources
This project uses geospatial datasets from **Comune di Trento Open Data** and **OpenStreetMap (OSM)**.

### 🏙️ Open Data - Comune di Trento  
Most datasets were sourced from the [Comune di Trento Open Data portal](https://www.comune.trento.it/Aree-tematiche/Open-Data), provided in GeoJSON format.

- **Trento Districts (`circoscrizioni`)**  
  Administrative boundaries of Trento’s **12 districts**, used for spatial aggregation.  

- **Bike Lanes (`bike_lanes`)**  
  Contains Trento’s **bike lanes and shared pedestrian-cyclist paths**, classified under municipal or provincial jurisdiction.  

- **Bike Parking (`bike_parking`)**  
  Information on **protected long-term bike parking areas**, including capacity and location.  

- **Bike Racks (`racks`)**  
  Maps **bike racks** in the limited traffic zone, categorized by type and capacity.  

- **Contour Lines (`elevation`)**  
  **Topographic contour lines** with a 10-meter vertical interval, derived from aerial surveys.  

### 🌐 OpenStreetMap Data  
Additional datasets were extracted using the `osmnx` library.

- **Natural Areas (`natural_areas`)**  
  Includes **parks and grassy areas**, retrieved by filtering OSM features tagged as `leisure=park` or `landuse=grass`.  

- **Points of Interest (`pois`)**  
  Diverse range of **urban amenities**, including shops, offices, and public services.  

- **Street Network (`streets`)**  
  The **road network** of Trento, extracted using `network_type="all"`.  

- **Pedestrian Network (`walkways`)**  
  The **walkable network**, including sidewalks, footpaths, and pedestrian streets (`network_type="walk"`).  

Each dataset was reprojected to **EPSG:32632 (WGS 84 / UTM zone 32N)** for spatial analysis.  


## 📊 Results  

### Bikeability Index  
![Bikeability Index](https://github.com/Ggenoni/Geospatial_analysis_and_representation/blob/main/images/bikability.png)  

### Pedestrian Network Intersection Density  
![Pedestrian Network Intersection Density](https://github.com/Ggenoni/Geospatial_analysis_and_representation/blob/main/images/network_intersection.png) 


## 📚 References  

- Haapanen, E. (2021). *Walkability Analysis*. Retrieved from [GitHub](https://github.com/eemilhaa/walkability-analysis). *(Last accessed: 2025-02-20)*  
- Gehring, D. (2016). *Bikeability-Index für Dresden – Wie fahrradfreundlich ist Dresden*. Master's thesis, Technische Universität Dresden, Professur für Verkehrsökologie. Available at: [Link](http://nbn-resolving.de/urn:nbn:de:bsz:14-qucosa-201073)  
- Hall, C. M., & Ram, Y. (2018). *Walk Score® and its potential contribution to the study of active transport and walkability: A critical and systematic review*.  
  *Transportation Research Part D: Transport and Environment, 61*, 310–324.  
  [DOI: 10.1016/j.trd.2017.12.018](https://doi.org/10.1016/j.trd.2017.12.018)  
- Abdelfattah, L., Deponte, D., & Fossa, G. (2022). *The 15-minute city as a hybrid model for Milan*.  
  *TeMA – Journal of Land Use, Mobility and Environment*, 71–86.  
- Moreno, C., Allam, Z., Chabaud, D., Gall, C., & Pratlong, F. (2021).  
  *Introducing the “15-Minute City”: Sustainability, Resilience and Place Identity in Future Post-Pandemic Cities*.  
  *Smart Cities, 4(1)*, 93–111.  
  [DOI: 10.3390/smartcities4010006](https://doi.org/10.3390/smartcities4010006)  
- Heinemann, M. (2022). *Radfreundlichkeit in der Stadt. Umsetzung eines Bikeability-Index auf Basis von OpenStreetMap am Beispiel Heidelberg*.  
  Heidelberg Institute for Geoinformation Technology, Geographie, Heidelberg.  
- Ewing, R., & Cervero, R. (2010). *Travel and the built environment: A meta-analysis*.  
  *Journal of the American Planning Association, 76(3)*, 265–294.  
  [DOI: 10.1080/01944361003766766](https://doi.org/10.1080/01944361003766766)  
- Novack, T., Wang, Z., & Zipf, A. (2018). *A system for generating customized pleasant pedestrian routes based on OpenStreetMap data*.  
  *Sensors, 18(11)*, 3794.  
  [DOI: 10.3390/s18113794](https://doi.org/10.3390/s18113794)  

