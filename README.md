# USGS Global Earthquake Exploratory Data Analysis (1900-2025)
![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Earthquake-EDA-1900-2025-/blob/main/Images/earthquake_new.png?raw=true) 
## 🌍 Project Overview

This project presents an in-depth Exploratory Data Analysis (EDA) of global earthquake activity from 1900 to 2025, using data sourced from the United States Geological Survey (USGS). The goal of this analysis is to uncover long-term seismic trends, geographical distributions, magnitude characteristics, and temporal patterns of earthquakes worldwide. Through Python-based visualization and geospatial analysis, this project aims to provide insights into the frequency, strength, and spatial behavior of earthquakes over the last 125 years, helping to better understand Earth’s seismic activity patterns. 

## 🗂️ Dataset 

While several region-specific earthquake datasets exist — such as the [Turkish Earthquake Dataset (1914–2023)](https://www.kaggle.com/datasets/ozgecinko/turkey-earthquake-data-1914-2023) , the [Italian INGV Dataset](https://www.pi.ingv.it/banche-dati/instance/) , and the [Stanford Earthquake Dataset](https://www.pi.ingv.it/banche-dati/instance/) ; the [USGS Global Dataset](https://www.kaggle.com/datasets/bwandowando/earthquakes-around-the-world-from-1900-2025/data) stands out as the most suitable foundation for a comprehensive, long-term, and comparative exploratory analysis. 

| **Aspect**              | **USGS Global Dataset**    | **Turkish Dataset**    | **Italian Dataset**     | **Stanford Dataset** |
| ----------------------- | -------------------------- | ---------------------- | ----------------------- | -------------------- |
| **Geographic Scope**    | Worldwide                  | Turkey only            | Italy only              | Regionally limited   |
| **Time Range**          | 1900–2025                  | 1914–2023              | 1985–present            | Varies               |
| **Data Source**         | USGS (authoritative)       | Kandilli Observatory   | INGV (Italy)            | Academic collection  |
| **Standardization**     | High (consistent schema)   | Moderate               | Moderate                | Varies               |
| **Best For**            | Global & comparative EDA   | Regional seismic focus | Regional hazard studies | Specialized research |
| **Chosen For Project?** | **Yes**                    | No                     | No                      | No                   | 

The [USGS Global Dataset](https://www.kaggle.com/datasets/bwandowando/earthquakes-around-the-world-from-1900-2025/data) provides the broadest, most consistent, and longest publicly available record of seismic activity. Its extensive temporal coverage (1900–2025) and standardized global reporting make it ideal for uncovering long-term trends and global-scale earthquake behavior. This enables richer insights across both time and geography, supporting research-grade EDA and global visualization. Summary of important columns of this dataset is given below. 

| **Column Name** | **Data Type**         | **Description**                                                                                             | **Example Value**     |
| --------------- | --------------------- | ----------------------------------------------------------------------------------------------------------- | --------------------- |
| `DateTime`      | `datetime`            | Timestamp of the earthquake occurrence in UTC. Enables time-series and trend analysis.                      | `2023-02-06 01:17:35` |
| `Latitude`      | `float`               | Geographic coordinate specifying the north–south position of the epicenter (in decimal degrees).            | `38.021`              |
| `Longitude`     | `float`               | Geographic coordinate specifying the east–west position of the epicenter (in decimal degrees).              | `37.204`              |
| `Depth`         | `float`               | Depth of the earthquake’s focus in kilometers below the surface. Helps analyze shallow vs deep earthquakes. | `10.0`                |
| `Magnitude`     | `float`               | Earthquake’s magnitude (Richter, Mw, or Ms), indicating energy released. Used for intensity classification. | `7.8`                 |
| `Type`          | `string`              | Type or classification of seismic event (e.g., Earthquake, Quarry Blast, Nuclear Explosion, Induced Event). | `Earthquake`          |
| `Location`      | `string`              | Nearest known place or region name describing where the earthquake occurred.                                | `Southern Turkey`     |
| `Country`       | `string`              | Country name derived from geographic coordinates or location metadata.                                      | `Turkey`              |
| `Source`        | `string`              | Data provider or recording agency (typically USGS).                                                         | `USGS`                |
| `Status`        | `string`              | Event verification status — indicates whether the event was reviewed or automatic.                          | `reviewed`            |





