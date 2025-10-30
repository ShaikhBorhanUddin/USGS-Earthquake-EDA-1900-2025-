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

Some columns have significant amount of missing values. These are visualized in the following bar chart. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/null_values.png?raw=true) 

## 🔍 Objectives

The analysis focuses on answering key questions such as:

- Which regions and countries experience the most earthquakes?

- How has earthquake frequency changed over time?

- What is the relationship between magnitude and depth?

- Which types of earthquakes are most common and most destructive?

- Are there observable global or regional patterns in seismic intensity?

## 📊 Key Exploratory Analyses 

🌍 **Which regions and countries experience the most earthquakes?** 

<p align="center">
  <img src="Images/world_map_new.png" alt="World Map" width="45.2%" />
  <img src="Images/continent.png" alt="Continent" width="53%" />
</p> 

The global earthquake distribution analysis from 1900 to 2025 reveals that seismic activity is highly concentrated along major tectonic plate boundaries, especially within the Pacific Ring of Fire. North America recorded the highest number of earthquakes, largely due to the high-frequency events in Alaska, the western United States, and along the Rocky Mountain region. Significant seismic clusters were also observed across the Andes Mountains in South America, the coastal regions of Japan, the South China Sea, the Indochinese Peninsula, and parts of Central and Southern Europe; all of which lie near active plate boundaries. Oceanic zones such as the Bismarck Sea, Philippine Sea, and other subduction zones around the Pacific were particularly active, highlighting the strong relationship between tectonic interactions and earthquake frequency. In contrast, vast inland regions like mainland Canada, Brazil, central Russia, and much of Africa exhibited relatively low seismic activity, while Antarctica remained the least affected continent. Although the **`place`** column in the dataset contains detailed location descriptors (e.g., “Yakutat Bay, Alaska” or “Bismarck Sea”), extracting specific country-level information from over four million records would require extensive geocoding computations. Therefore, this analysis emphasizes continental and regional patterns rather than individual country counts. 

🕰️ **How has earthquake frequency changed over time?** 

<p align="center">
  <img src="Images/yearly_trend.png" alt="Yearly Trend" width="32%" />
  <img src="Images/5_year_rolling_avg.jpg" alt="5 Year Rolling Average" width="32%" />
  <img src="Images/monthly_frequency.png" alt="Monthly Frequency" width="34%" />
</p>  

The frequency of earthquakes has changed dramatically over the past century. From 1900 to about 1970, the recorded number of earthquakes was very low, largely because of limited global coverage and the lack of advanced seismic monitoring equipment. As technology improved and seismic networks expanded worldwide after the 1970s, there was a noticeable and steady increase in the number of recorded earthquakes. This upward trend continued into the 2000s, reaching its peak around 2015–2020, before showing a slight decline in recent years. The 5-year rolling average graph clearly illustrates this overall long-term growth and helps smooth out short-term fluctuations, confirming that the apparent surge is part of a consistent trend rather than random variation. The monthly frequency analysis also reveals seasonal differences, with July experiencing the highest number of earthquakes and February the lowest, although such variations are relatively modest compared to the broader upward trend over the decades. Overall, the data suggests that the observed increase in earthquake frequency is largely due to improved detection and reporting capabilities rather than a sudden rise in global seismic activity. 

📏 **At what depths do earthquakes occur most frequently, and are low-magnitude earthquakes more common than high-magnitude ones?** 

<p align="center">
  <img src="Images/depth.png" alt="Depth" width="48%" />
  <img src="Images/magnitude.png" alt="Magnitude" width="50.5%" />
</p> 

The graphs show that earthquakes occur most frequently at very shallow depths, especially in the −10 to 16 km range. The presence of negative depth values indicates that many of these events happen extremely close to the Earth’s surface, sometimes even slightly above the reference level used for measuring depth. As depth increases, the frequency of earthquakes declines sharply, showing that deep earthquakes are much less common. Similarly, for magnitudes, the highest number of earthquakes occurs within the 0–2 magnitude range, but this also includes many events with slightly negative magnitudes. These negative-magnitude earthquakes are extremely small, often only detectable by instruments. The frequency drops steadily as the magnitude increases, with large earthquakes (above magnitude 6) being very rare. Overall, the data reveal that the most common earthquakes are both shallow (often near or just above the reference surface) and of very low magnitude, meaning that most seismic activity worldwide consists of tiny, surface-level tremors.




## Work on Progress 
🌍 1. Temporal Analysis

Goal: Understand how earthquake activity evolved over time.

Line Chart: Yearly trend of earthquakes (time column → extract year).

Line Chart (Stacked or Multi-line): Yearly average magnitude by continent or by type.

Rolling Average (e.g., 5-year): Smooth the time trend to show long-term seismic activity patterns. 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/yearly_trend.png?raw=true) 

![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/5_year_rolling_avg.jpg?raw=true) 

<p align="center">
  <img src="Images/yearly_trend.png" alt="Average Valuation by Industry" width="52%" />
  <img src="Images/5_year_rolling_avg.jpg" alt="Top Funding-to-Valuation Ratios" width="47.1%" />
</p>

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
![Dashboard](https://github.com/ShaikhBorhanUddin/USGS-Global-Earthquake-Exploratory-Data-Analysis-1900-2025/blob/main/Images/world_map.png?raw=true)





