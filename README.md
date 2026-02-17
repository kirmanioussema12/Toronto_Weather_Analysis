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

## 📁 Project Structure

```text
Toronto_Weather_Analysis/
│
├── Assignment-1.ipynb
├── TORONTO_INTL_A_Climate_Daily_Data_2025.csv
└── README.md
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



