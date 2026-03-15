# 🌦️ Toronto Weather Analysis (2025)  
### 📊 Daily Climate Data Exploration — Built with Pure Python

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![Dataset](https://img.shields.io/badge/Dataset-CSV-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

---

## ✨ Overview

This project analyzes **daily climate data for Toronto International Airport (2025)** using **pure Python only** — without relying on external libraries such as **Pandas**, **NumPy**, or **Matplotlib**.

The goal of this notebook is to practice:

- 📥 Manual dataset loading  
- 🧹 Cleaning real-world climate data  
- 📊 Performing statistics from scratch  
- 📈 Extracting useful weather insights  
- 🧠 Strengthening Python fundamentals  

---

## 📌 Table of Contents

- [✨ Overview](#-overview)
- [🛠️ Technologies Used](#️-technologies-used)
- [📁 Project Structure](#-project-structure)
- [📊 Dataset Description](#-dataset-description)
- [🧠 Notebook Workflow](#-notebook-workflow)
- [📈 Results & Insights](#-results--insights)
- [🖼️ Screenshots](#️-screenshots)
- [▶️ How to Run](#️-how-to-run)
- [🌍 Real-World Relevance](#-real-world-relevance)
- [👨‍💻 Author](#-author)
- [⭐ Support](#-support)

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| 🐍 Python | Core data processing & analysis |
| 📓 Jupyter Notebook | Interactive notebook environment |
| 📄 CSV Dataset | Raw climate data |

⚠️ **Important:**  
This project was intentionally built with **pure Python only**, meaning:

✅ No Pandas  
✅ No NumPy  
✅ No Matplotlib  
✅ No built-in data science libraries  

Everything is implemented using:

- File handling (`open`, `readlines`)  
- String operations (`split`, `strip`)  
- Loops and conditionals  
- Lists and dictionaries  
- Manual numeric conversion (`float`, `int`)  

---
## 📊 About the Data

This dataset contains **daily weather observations** from **Toronto Pearson International Airport (TORONTO INTL A)** for the full year **2025**.  
- **Station**: Toronto Pearson International Airport  
- **Climate ID**: 6158731  
- **Coordinates**: Longitude -79.63°, Latitude 43.68°  
- **Time coverage**: January 1, 2025 – December 31, 2025 (365 days)  
- **Source style**: Environment and Climate Change Canada (ECCC) daily climate summary format

### Main Columns Explained

| Column Name              | Data Type       | Description                                                                 | Unit / Range / Notes                                      | Typical Values (from 2025 data)                     |
|--------------------------|-----------------|-----------------------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------|
| Longitude (x)            | Float           | Longitude coordinate of the station                                         | Degrees                                                   | Always -79.63                                       |
| Latitude (y)             | Float           | Latitude coordinate of the station                                          | Degrees                                                   | Always 43.68                                        |
| Station Name             | String          | Name of the weather station                                                 | —                                                         | Always "TORONTO INTL A"                             |
| Climate ID               | Integer/String  | Official ECCC climate station identifier                                    | —                                                         | Always 6158731                                      |
| Date/Time                | String (ISO)    | Full date of the observation                                                | YYYY-MM-DD                                                | 2025-01-01 to 2025-12-31                            |
| Year                     | Integer         | Year of the observation                                                     | —                                                         | Always 2025                                         |
| Month                    | Integer         | Month (1–12)                                                                | —                                                         | 1 to 12                                             |
| Day                      | Integer         | Day of the month (1–31)                                                     | —                                                         | 1 to 31                                             |
| Max Temp (°C)            | Float           | Highest temperature recorded during the day                                 | °C                                                        | -10.6 to 14.1 (Jan–Nov sample)                      |
| Min Temp (°C)            | Float           | Lowest temperature recorded during the day                                  | °C                                                        | -18.5 to 5.1                                        |
| Mean Temp (°C)           | Float           | (Max + Min) / 2                                                             | °C                                                        | -14.0 to 8.5                                        |
| Heat Deg Days (°C)       | Float           | Heating degree days (base 18°C) – measure of heating demand                 | °C-days                                                   | 9.5 to 32.0 (higher in winter)                      |
| Cool Deg Days (°C)       | Float           | Cooling degree days (base 18°C) – measure of cooling demand                 | °C-days                                                   | Almost always 0 in 2025 sample (cold year?)         |
| Total Rain (mm)          | Float           | Total rainfall measured                                                     | mm                                                        | 0 to 41.2 (very high on Dec 28)                     |
| Total Snow (cm)          | Float           | Total snowfall measured                                                     | cm                                                        | 0 to 17.4 (mostly winter months)                    |
| Total Precip (mm)        | Float           | Total precipitation (rain + liquid water equivalent of snow)               | mm                                                        | 0 to 41.2                                           |
| Snow on Grnd (cm)        | Float / Empty   | Depth of snow on the ground at observation time                             | cm                                                        | 0 to 8 (missing on many days)                       |
| Dir of Max Gust (10s deg)| Integer / Empty | Direction of the maximum wind gust (in tens of degrees)                     | 0–36 (10° increments), or empty                           | 0–50 (missing on calm days)                         |
| Spd of Max Gust (km/h)   | Integer / Empty | Speed of the maximum wind gust during the day                               | km/h                                                      | 20–85 (missing on calm days)                        |

**Key Observations from the 2025 Data**
- Temperatures are generally **cool** — many winter days below -10°C, summer months not shown in sample but appear mild.
- **Precipitation** is mixed: rain in warmer months, snow in winter.
- **Cooling degree days** are 0 in the provided sample — suggests a cooler-than-average year or early/late season data.
- Many **gust direction/speed** fields are empty on calm days.
- Snow on the ground is sparsely reported (many blanks).
- Extreme values: highest rain 41.2 mm (Dec 28), highest gust 85 km/h (Feb 6).

You can load and explore the full file with:

```python
import pandas as pd

df = pd.read_csv("TORONTO_INTL_A_Climate_Daily_Data_2025 (1).csv")
print(df.info())
print(df.describe())
print("Monthly average temperature:")
print(df.groupby('Month')['Mean Temp (°C)'].mean())
```
---

## 📁 Project Structure

```text
Toronto_Weather_Analysis/
│
├── Assignment-1.ipynb
├── TORONTO_INTL_A_Climate_Daily_Data_2025.csv
└── README.md
```
---
## 📄 Dataset Description

**Dataset File:**  
`TORONTO_INTL_A_Climate_Daily_Data_2025.csv`

**Location:**  
Toronto International Airport (Toronto, Canada)

**Time Period:**  
January 2025 → December 2025
---
### 🔎 What the Dataset Contains

Daily climate measurements including:

- 📅 **Date**
- 🌡️ **Maximum Temperature** (°C)
- 🌡️ **Minimum Temperature** (°C)
- 🌡️ **Mean Temperature** (°C)
- 🌧️ **Total Rain** (mm)
- ❄️ **Snowfall** (cm) (when applicable)
- 💨 **Wind Speed**
- 🌫️ Additional atmospheric indicators (depending on record)

### 📌 Why This Dataset Is Useful

Perfect for:

- 🌡️ Temperature trend analysis
- 🌧️ Precipitation pattern detection
- ❄️ Identifying extreme weather days
- 📊 Practicing real-world data analysis
- 🧠 Strengthening data preprocessing skills

## 🧠 Notebook Workflow

This project follows a **full mini data science pipeline** using **only core Python** (no pandas, numpy, etc.).

1. **Data Loading (Manual CSV Parsing)**  
   - Opens file with Python file handling  
   - Reads CSV line-by-line  
   - Extracts headers and rows manually  
   - Stores data in Python lists / dictionaries

2. **Data Cleaning & Preprocessing**  
   - Removes empty/invalid values  
   - Handles missing or malformed measurements  
   - Converts strings to numeric values  
   - Ensures data consistency

3. **Statistical Analysis**  
   - Average temperature calculations  
   - Maximum / minimum temperature detection  
   - Total precipitation computation  
   - Monthly summaries  
   - Extreme weather day identification

4. **Insight Generation**  
   Answers questions such as:

   - 🔥 What was the **hottest** day in 2025?
   - ❄️ What was the **coldest** day in 2025?
   - 🌧️ What was the **rainiest** day?
   - 📆 Which month was the **warmest** overall?
   - 📉 How does temperature vary across the year?

## 📈 Results & Insights

(Values to be filled after running the notebook)

- 🔥 **Hottest Day:** YYYY-MM-DD — XX.X °C  
- ❄️ **Coldest Day:** YYYY-MM-DD — XX.X °C  
- 🌧️ **Rainiest Day:** YYYY-MM-DD — XX.X mm  
- 📆 **Warmest Month:** Month Name  
- 📆 **Coldest Month:** Month Name  
- 🌡️ **Yearly Mean Temperature:** XX.X °C  
- 🌧️ **Total Precipitation (Year):** XXX.X mm  



