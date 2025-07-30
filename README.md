# 📘 Kolkata Climate Analysis (1951 – 2020)

## 🔍 Project Objective

This Power BI report provides a detailed and interactive visualization of **Kolkata’s climate trends from 1951 to 2020**.  
It helps users explore long-term patterns in temperature, rainfall, and seasonal changes — supporting **climate research**, **urban planning**, and **environmental decision-making**.

---

## 📁 Dataset Overview

- **Source Format**: CSV  
- **Location Covered**: Kolkata  
- **Time Period**: 1951 to 2020  
- **Columns in Dataset**:
  - `date`  
  - `temp_max`  
  - `temp_min`  
  - `rain`

---

## ✅ Data Cleaning & Transformation (Using DAX in Power BI)

### 🔧 New Columns Created

| Column Name     | Description                                     |
|------------------|-------------------------------------------------|
| Avg Temp         | (`temp_max` + `temp_min`) / 2 — Daily average temperature |
| Temp Range       | `temp_max` - `temp_min` — Shows daily temperature fluctuation |
| Rain Category    | Categorized rainfall based on intensity         |

### 🧠 Rain Category Logic (DAX)

```DAX
Rain Category = 
SWITCH(
    TRUE(),
    'Kolkata'[rain] = 0, "No Rain",
    'Kolkata'[rain] <= 2, "Light",
    'Kolkata'[rain] <= 10, "Moderate",
    "Heavy"
)
```

---

## 🗓️ Date Table (Custom Created in Power BI)

| Column Name   | Use Case                            |
|---------------|-------------------------------------|
| Date          | Creates relationship with main table |
| Year          | Enables year-wise filters            |
| Month         | Used for monthly slicer              |
| Month Number  | Ensures correct sorting              |
| Month-Year    | Used for monthly trend charts        |

---

## 🛠️ Project Workflow Summary

- Imported the CSV dataset into Power BI  
- Cleaned column names and fixed data types  
- Created calculated columns for:
  - Avg Temp  
  - Temp Range  
  - Rain Category  
- Built and linked a custom Date Table  
- Designed interactive visuals using:
  - Charts  
  - KPIs  
  - Slicers  
- Finalized dashboard layout for clear storytelling

---

## 📊 Final Dashboard Components

| Component         | Description                                            |
|-------------------|--------------------------------------------------------|
| KPI Cards         | Shows Total Rain, Avg Rain, Avg Max Temp, Avg Min Temp, Avg Temp |
| Line Chart        | Avg Temp trend from 1951 to 2020                       |
| Clustered Line    | Max vs Min Temp across years                           |
| Pie Chart         | Rain Category distribution                             |
| Matrix Table      | Count of rain types: No Rain, Light, Moderate, Heavy   |
| Bar Chart         | Monthly Rainfall trends in recent years                |
| Slicers           | Filter by Year, Month, and Rain Category               |

---

## 🔍 Insights Derived from the Dashboard

| Analysis Point             | Insight Description                                          |
|----------------------------|--------------------------------------------------------------|
| 🌧️ Total & Avg Rainfall     | Track how overall rainfall changed over the decades         |
| 🌡️ Avg Max/Min Temperature | Understand seasonal patterns and warming trends             |
| 📅 Monthly Rainfall Trends | Detect driest/wettest months through time                   |
| 🌀 Rain Category Distribution | Learn frequency of Heavy, Moderate, Light, and No Rain    |
| 🕒 Temperature Range Trend  | See how daily fluctuations evolved                           |
| 🔍 Avg Temp Observations   | Check consistency and changes in average comfort level       |
| ⛅ Avg of Avg Temp         | Get a general idea of city weather comfort over time         |
| 📉 Rain vs Temperature     | Explore inverse or correlated relationships visually         |

---

## 🚀 How to Explore the Report

- Use the **Year and Month slicers** to focus on specific periods  
- Hover on **charts** to see exact values and trends  
- Use **Rain Category filter** to study rain intensity  
- Compare **Max vs Min Temperature trends** to detect long-term climate shifts  
- Explore **Monthly Rainfall bar chart** to analyze seasonality and anomalies

---

