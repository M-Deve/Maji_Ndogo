# 🌾 Maji Ndogo: Farming Automation Data Analysis

Welcome to the Maji Ndogo project — an ambitious data analysis initiative supporting the automation of agriculture in a diverse and challenging landscape. This project lays the groundwork for making informed decisions about where and what to farm by analyzing environmental, geographic, and crop-related data.

## 📌 Project Overview

Maji Ndogo, a region with varied terrain and climate conditions, is on a mission to revolutionize agriculture using data. Before deploying automation tools, it is crucial to understand:

- 🌱 Where to farm  
- 🌾 What to grow  
- 🌤️ Which environmental conditions influence yields  

Our job? Combine and clean data from multiple tables in an SQLite database, explore patterns and correlations, and produce actionable insights.

---

## 🗃️ Data Sources

The data is stored in an SQLite database: `Maji_Ndogo_farm_survey.db`. It consists of four tables joined by the common field: `Field_ID`.

### 1. 🌍 Geographic Features

| Column    | Description                                         |
|-----------|-----------------------------------------------------|
| Field_ID  | Unique field identifier (BigInt)                    |
| Elevation | Elevation in meters (Float)                         |
| Latitude  | Latitude in degrees (Float)                         |
| Longitude | Longitude in degrees (Float)                        |
| Location  | Province or administrative region (Text)           |
| Slope     | Land slope (Float)                                  |

### 2. 🌦️ Weather Features

| Column             | Description                                  |
|--------------------|----------------------------------------------|
| Field_ID           | Field identifier (BigInt)                    |
| Rainfall           | Annual rainfall in mm (Float)               |
| Min_temperature_C  | Avg. minimum temperature in °C (Float)      |
| Max_temperature_C  | Avg. maximum temperature in °C (Float)      |
| Ave_temps          | Average temperature in °C (Float)           |

### 3. 🌱 Soil and Crop Features

| Column         | Description                                              |
|----------------|----------------------------------------------------------|
| Field_ID       | Field identifier (BigInt)                                |
| Soil_fertility | Fertility score from 0 (infertile) to 1 (very fertile)  |
| Soil_type      | Soil classification (Text)                               |
| pH             | Soil pH value (Float)                                    |

### 4. 🧑‍🌾 Farm Management Features

| Column          | Description                                                               |
|-----------------|---------------------------------------------------------------------------|
| Field_ID        | Field identifier (BigInt)                                                 |
| Pollution_level | Pollution level (0 = unpolluted, 1 = very polluted) (Float)               |
| Plot_size       | Field area in hectares (Float)                                            |
| Chosen_crop     | Crop type cultivated (Text)                                               |
| Annual_yield    | Total annual yield (Float)                                                |
| Standard_yield  | Normalized yield value (Float)                                            |

---

## 🔍 Analysis Process

The main steps in this project include:

1. 📥 Importing Data:  
   - Load multiple tables from SQLite and join on Field_ID  
   - Convert data to a unified Pandas DataFrame for analysis  

2. 🧹 Data Cleaning:  
   - Handle missing or inconsistent data  
   - Normalize values where necessary  
   - Prepare categorical variables for analysis  

3. 📊 Exploratory Data Analysis:  
   - Correlation analysis between features and yield  
   - Visualizing environmental conditions and crop choices  
   - Identifying optimal planting zones based on fertility, rainfall, etc.  

4. 📈 Insights & Recommendations:  
   - Which regions are best for specific crops  
   - What environmental factors most affect yield  
   - Suggestions for maximizing output while minimizing input  

---

## 👤 Author

**[Moyinoluwa Adisa]**  
Aspiring Data Engineer | Python & SQL Enthusiast  
GitHub: (https://github.com/M-Deve)  
LinkedIn: (https://linkedin.com/in/moyinoluwaadisa)  
Email: adisamoyin@gmail.com
