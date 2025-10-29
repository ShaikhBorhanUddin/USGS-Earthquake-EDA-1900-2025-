# USGS Global Earthquake Exploratory Data Analysis (1900-2025) 
<p align="left">
  <img src="https://img.shields.io/badge/Made%20With-Colab-blue?logo=googlecolab&logoColor=white&label=Made%20With" alt="Made with Colab">
  <img src="https://img.shields.io/badge/Data%20Visualization-Matplotlib%20%7C%20Seaborn%20%7C%20Folium-yellow?logo=python&logoColor=white" alt="Data Visualization">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT">
  <img src="https://img.shields.io/github/repo-size/ShaikhBorhanUddin/EDA-of-Nigerian-Road-Traffic-Crashes-2020-2024" alt="Repo Size">
  <img src="https://img.shields.io/github/last-commit/ShaikhBorhanUddin/EDA-of-Nigerian-Road-Traffic-Crashes-2020-2024" alt="Last Commit">
  <img src="https://img.shields.io/github/issues/ShaikhBorhanUddin/EDA-of-Nigerian-Road-Traffic-Crashes-2020-2024" alt="Issues">
  <img src="https://img.shields.io/badge/Host-GitHub-black?logo=github" alt="Host: GitHub">
  <img src="https://img.shields.io/badge/Version%20Control-Git-orange?logo=git" alt="Version Control: Git">
  <img src="https://img.shields.io/badge/Project-Ongoing-blueviolet" alt="Project Status">
</p>

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
| `Status`        | `string`              | Event verification status (indicates whether the event was reviewed or automatic)                           | `reviewed`            |

## Work on Progress 
🌍 1. Temporal Analysis

Goal: Understand how earthquake activity evolved over time.

Line Chart: Yearly trend of earthquakes (time column → extract year).

Line Chart (Stacked or Multi-line): Yearly average magnitude by continent or by type.

Rolling Average (e.g., 5-year): Smooth the time trend to show long-term seismic activity patterns. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/yearly_trend.png?raw=true) 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/5_year_rolling_avg.jpg?raw=true) 



🕰️ 2. Time of Day & Month Patterns

Goal: See if earthquakes have temporal concentration.

Histogram: Distribution by hour of the day (convert UTC time → hour).

Bar Chart: Monthly frequency of earthquakes across years. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/monthly_frequency.png?raw=true)

📊 3. Depth vs Magnitude Relationship

Goal: Examine how earthquake depth relates to magnitude.

Scatter Plot: depth vs mag, colored by type or continent.

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/depth_vs_mag.png?raw=true) 

Correlation Heatmap: Include mag, depth, and rms (if available). 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/heatmap.png?raw=true)

🗺️ 4. Global Heatmap (Geospatial Visualization)

Goal: Visualize where earthquakes are concentrated geographically.

Folium Map / Plotly Mapbox:

Plot all earthquakes (latitude, longitude) sized by magnitude and colored by depth. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/world_map_new.png?raw=true) 

Optionally, create a choropleth showing the average magnitude by country.

⚙️ 5. Magnitude and Depth Classification

Goal: Categorize and summarize earthquake severity. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/depth.png?raw=true) 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/magnitude.png?raw=true) 

Create bins (e.g., Minor: <4, Light: 4–5, Moderate: 5–6, Strong: 6–7, Major: 7+).

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/earthquake_category.png?raw=true) 

Stacked Bar Chart: Number of earthquakes per category by continent or decade.

🌐 6. Continent or Region-Level Insights

Goal: Summarize seismic activity geographically. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/continent.png?raw=true) 

Treemap: Total number of earthquakes per continent → subdivided by country.

Box Plot: Magnitude by continent.

🧭 7. Top N Analyses

Goal: Identify key outliers and extreme events.

Table + Highlighted Bar: Top 10 strongest earthquakes (with date, place, magnitude, depth).

Map Markers: Pin only top 10 earthquakes globally. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/top_10_highest_magnitude.png?raw=true) 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/top_10_with_time.png?raw=true) 

⚠️ 8. Seismic Frequency Over Decades

Goal: Observe change in detection and reporting.

Bar Chart: Count of earthquakes per decade.

Overlay Line: Mean magnitude per decade. 

🧩 9. Correlation and Statistical Summary

Goal: Summarize numeric patterns.

Pairplot (Seaborn): Show pairwise relationships among mag, depth, rms, etc. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/pairplot.png?raw=true) 

Correlation Matrix Heatmap. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/heatmap_numerical.png?raw=true)

🧮 10. Advanced Insight (optional)

Goal: Add analytical depth.

Clustering (KMeans) of earthquakes based on mag, depth, latitude, longitude → to find seismic zones.

Anomaly Detection: Identify unusually shallow or deep strong earthquakes.
![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/null_values.png?raw=true)
![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/world_map.png?raw=true)





