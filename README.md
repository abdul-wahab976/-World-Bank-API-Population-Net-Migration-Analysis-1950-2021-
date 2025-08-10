# 🌍 World Bank API – Population & Net Migration Analysis (1950–2021)

---

## 📖 Introduction
This project demonstrates how to **scrape and analyze global development data** directly from the **World Bank API** using Python.  
By connecting to the API via the `wbdata` library, the script automatically fetches, cleans, and explores **total population** and **net migration** data for selected countries, covering the period **1950–2021**.

It is a **fully reproducible workflow** that transforms raw API data into meaningful insights through:
- **Automated data acquisition**
- **Systematic cleaning and preprocessing**
- **Exploratory Data Analysis (EDA)**
- **Statistical summaries**
- **High-quality visualizations**

---

## 🎯 Project Purpose
The aim is to build a **data pipeline** that:
1. **Scrapes** structured time-series data from the **World Bank API**.
2. **Cleans and filters** the dataset for relevant years and countries.
3. **Analyzes** population growth and migration patterns.
4. **Visualizes** findings through clear, insightful charts.
5. **Saves outputs** for reporting and reuse.

---

## 🔢 Data Source & Indicators
The data is scraped in real-time from the [World Bank Open Data API](https://data.worldbank.org/) via `wbdata`.  

**Indicators used:**
| **Code**        | **Name in Script**   | **Description** |
|-----------------|----------------------|-----------------|
| `SP.POP.TOTL`   | `Total_Population`   | Total population of a country (all ages, all residents). |
| `SM.POP.NETM`   | `Net_Migration`      | Net migration (immigrants minus emigrants) in a given year. |

**Countries included:**  
India (IN), Pakistan (PK), Bangladesh (BD), Sri Lanka (LK), Afghanistan (AF), New Zealand (NZ), Saudi Arabia (SA)

---

## 🛠 Behaviours in the Script
| **Step** | **Behaviour** | **Details** |
|----------|--------------|-------------|
| **1. API Data Fetch** | Real-time scraping | Uses `wbdata.get_dataframe()` to fetch two World Bank indicators for specified countries. |
| **2. Data Cleaning** | Formatting & filtering | Converts `Year` to numeric, filters 1950–2021, renames columns, resets index. |
| **3. CSV Export** | Save processed data | Saves cleaned dataset to `Population_&_Navigatore.csv` for offline use. |
| **4. Data Overview** | EDA basics | Prints `info()`, summary statistics, and missing value counts. |
| **5. Population Trends** | Time-series line plot | Plots population growth for each country over time. |
| **6. Latest Year Comparison** | Bar chart | Shows population by country in the most recent year available. |
| **7. Average Net Migration** | Aggregation & bar plot | Calculates mean net migration and plots results. |
| **8. Correlation Analysis** | Heatmap | Displays correlation between population and migration. |
| **9. Organized Outputs** | Figures & tables | Saves plots to `outputs/figures/` and summary tables to `outputs/results/`. |

---


