# 🦠 COVID-19 Analytics Dashboard

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-013243?style=flat-square&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-4c72b0?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter)

A comprehensive data analysis project focused on understanding the global impact of COVID-19 through data cleaning, preprocessing, exploratory data analysis (EDA), statistical insights, and rich visualizations — covering both **global trends** and **India-specific analysis**.

---

## 📌 Project Overview

The COVID-19 pandemic generated massive amounts of public health data worldwide. This project analyzes real-world datasets to identify patterns, trends, and correlations that support data-driven understanding of the pandemic.

**Key Objectives:**

- 🧹 Data Cleaning & Preprocessing (missing values, type conversion, feature engineering)
- 📊 Exploratory Data Analysis (EDA)
- 📈 Trend & Growth Rate Analysis
- 🔬 Statistical Insights & Correlation Analysis
- 🌍 Country-wise Comparative Analysis
- 🇮🇳 India State-wise Deep Dive

---

## 🚀 Technologies Used

| Technology       | Version  | Purpose                        |
| ---------------- | -------- | ------------------------------ |
| Python           | 3.8+     | Core programming language      |
| Pandas           | latest   | Data manipulation & cleaning   |
| NumPy            | latest   | Numerical computation & stats  |
| Matplotlib       | latest   | Charts, plots & visualizations |
| Seaborn          | latest   | Statistical visualizations     |
| Jupyter Notebook | latest   | Development environment        |
| OpenPyXL         | latest   | Reading Excel files            |

---

## 📂 Dataset Details

### Global CSV Datasets (`data/`)

| File | Rows | Columns | Description |
|------|------|---------|-------------|
| `recent_covid_19_data.csv` | 7,313 | 8 | Primary global dataset — 191 countries, Jan–Mar 2020 |
| `time-series-19-covid-combined.csv` | 25,760 | 8 | Daily time-series for all countries |
| `time_series_covid_19_confirmed.csv` | 442 | 57 | Wide-format confirmed cases by country |
| `time_series_covid_19_deaths.csv` | 442 | 57 | Wide-format deaths by country |
| `time_series_covid_19_recovered.csv` | 442 | 57 | Wide-format recoveries by country |

### India Excel Datasets (`excel/`)

| File | Rows | Description |
|------|------|-------------|
| `Covid cases in India.xlsx` | 26 | State-wise confirmed, cured & death counts |
| `Indian Coordinates.xlsx` | 35 | Latitude & longitude for Indian states |
| `per_day_cases.xlsx` | 52 | India daily new cases & cumulative totals |

### Dataset Features

- Country / Region & Province / State
- Confirmed, Active, Recovered & Death counts
- Date-wise records (Jan 22, 2020 → Mar 20, 2020)
- Derived features: `Active Cases`, `Mortality Rate (%)`, `Recovery Rate (%)`

---

## 📊 Analysis Performed

### 🧹 Data Cleaning
- Handling missing values (`Province/State` filled from `Country/Region`)
- Removing duplicate records
- Mixed-format datetime conversion
- Numeric type enforcement
- Feature engineering: `Active = Confirmed − Deaths − Recovered`

### 📐 Descriptive Statistics (NumPy + Pandas)
- Global totals: confirmed, deaths, recovered, active
- Mean, median, std deviation, percentiles via NumPy
- Per-country `.describe()` summary

### 🔍 Exploratory Data Analysis
- Infection & recovery trends over time
- Mortality analysis across countries
- Daily growth rate calculation with rolling averages
- Country-wise and region-wise comparisons
- India state-wise breakdown with coordinates

### 🔬 Statistical Analysis
- Correlation matrix (Confirmed ↔ Deaths ↔ Recovered ↔ Active)
- NumPy `polyfit` linear regression (log-log confirmed vs deaths)
- KDE & distribution analysis of case counts and rates
- Log-scale pandemic trajectory comparison

---

## 📈 Visualizations (18 Sections)

| # | Chart Type | Description |
|---|-----------|-------------|
| 5 | Grouped Bar | Top 15 countries — Confirmed, Deaths, Recovered, Active |
| 6 | Donut Pie + Horizontal Bar | Global distribution of all case types |
| 7 | Line + Bar (dual panel) | Global cumulative trend & daily new cases |
| 8 | Grouped Bar | Top 10 countries comparison |
| 9 | Seaborn Barplot | Mortality & Recovery rates (top countries) |
| 10 | Seaborn Heatmap | Correlation matrix |
| 11 | Line + Semi-log | Daily growth rate + log-scale confirmed trend |
| 12 | Multi-line | Pandemic trajectories — Top 8 countries |
| 13 | Stacked Horizontal Bar | India state-wise breakdown |
| 14 | Line + Bar (dual panel) | India daily cases + 7-day rolling average |
| 15 | Bubble Scatter Map | India geographic distribution (lat/long) |
| 16 | Seaborn Heatmap | India weekly case intensity (day × week pivot) |
| 17 | Hist / KDE / Box / Scatter | Statistical distributions & regression |

---

## 🔍 Key Insights

- 🌍 Identified countries with the highest infection, mortality, and recovery rates
- 📈 Visualized exponential pandemic growth using time-series and log-scale analysis
- 🔗 Strong positive correlation (`r > 0.95`) between Confirmed cases and Deaths
- 📉 Daily growth rate declined after initial peak — visible in 3-day smoothed trend
- 🇮🇳 Maharashtra & Delhi were India's most affected states during the study period
- 🗺️ Geographic bubble map reveals concentration of cases in major metro states

---

## 📁 Project Structure

```
COVID-19-Data-Analytics/
│
├── data/
│   ├── recent_covid_19_data.csv
│   ├── time-series-19-covid-combined.csv
│   ├── time_series_covid_19_confirmed.csv
│   ├── time_series_covid_19_deaths.csv
│   └── time_series_covid_19_recovered.csv
│
├── excel/
│   ├── Covid cases in India.xlsx
│   ├── Indian Coordinates.xlsx
│   └── per_day_cases.xlsx
│
├── notebooks/
│   └── Covid19-Data Analysis.ipynb   ← Main analysis notebook
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

**1. Clone the repository:**

```bash
git clone https://github.com/vatsalgajera-tech/COVID-19-Data-Analytics.git
cd COVID-19-Data-Analytics
```

**2. Install dependencies:**

```bash
pip install -r requirements.txt
```

**3. Launch Jupyter Notebook:**

```bash
jupyter notebook
```

**4. Open the notebook:**

Navigate to `notebooks/Covid19-Data Analysis.ipynb` and run all cells (`Kernel → Restart & Run All`).

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
jupyter
openpyxl
```

---

## 📌 Future Enhancements

- [ ] Interactive Dashboard using Streamlit or Plotly Dash
- [ ] Real-Time COVID Data Integration via public APIs
- [ ] Predictive Analysis using Machine Learning (ARIMA, LSTM)
- [ ] Choropleth Geographical Mapping (Folium / GeoPandas)
- [ ] Automated Report Generation (PDF export)
- [ ] Vaccination Progress Analysis

---

## 👨‍💻 Author

**Vatsal Gajera**

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!
