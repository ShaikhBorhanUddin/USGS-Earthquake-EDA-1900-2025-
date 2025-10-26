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

| Column        | Description                                                              |
| ------------- | ------------------------------------------------------------------------ |
| **time**      | Timestamp of the earthquake occurrence (UTC).                            |
| **latitude**  | Geographic coordinate (north–south position) of the epicenter.           |
| **longitude** | Geographic coordinate (east–west position) of the epicenter.             |
| **depth**     | Depth of the earthquake focus below the Earth’s surface (in km).         |
| **mag**       | Earthquake magnitude, measured on the Richter or moment magnitude scale. |
| **magType**   | Method used to calculate magnitude (e.g., mb, Mw, ML).                   |
| **nst**       | Number of seismic stations that recorded the event.                      |
| **gap**       | Azimuthal gap between stations (indicator of coverage quality).          |
| **dmin**      | Horizontal distance from the nearest station (in degrees).               |
| **rms**       | Root Mean Square (RMS) of travel time residuals.                         |
| **place**     | Textual description of the nearest location or region.                   |
| **type**      | Type of seismic event (e.g., earthquake, quarry blast, explosion).       |
| **id**        | Unique event identifier.                                                 | 



