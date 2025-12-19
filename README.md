# 🌍 ETL Project: Population & CO₂ Analytics Pipeline

This project demonstrates a **complete ETL pipeline** built in **Databricks Community Edition** using **PySpark**.  
It follows **data engineering best practices** and is designed to be **GitHub-friendly** for portfolio and interview purposes.

The pipeline integrates **population** and **CO₂ emissions** data to produce analytics-ready datasets using the **Medallion Architecture (Bronze → Silver → Gold)**.

---

## 🚀 Project Overview

- **Objective:**  
  Ingest population and CO₂ emissions data from public datasets, clean and transform the data, and generate analytical metrics such as **CO₂ emissions per 1,000 people**.

- **Architecture:**  
  Medallion (Bronze / Silver / Gold)

- **Technologies:**  
  - Databricks Community Edition  
  - PySpark  
  - Delta Lake  

- **Execution Environment:**  
  Databricks Free Edition 

---

## 🧱 Architecture Breakdown

### 🥉 Bronze Layer – Raw Ingestion
- Reads raw CSV files from DBFS  
- Applies schema inference  
- Stores raw data as Delta tables  

### 🥈 Silver Layer – Clean & Transform
- Renames columns for consistency  
- Casts data types  
- Filters and selects relevant fields  

### 🥇 Gold Layer – Analytics
- Joins population and CO₂ datasets by **country and year**  
- Computes derived metrics (e.g. CO₂ per 1,000 people)  
- Produces analytics-ready Delta tables  

---

## 📁 Repository Structure

```
etl-databricks-pyspark/
├─ notebooks/
│ ├─ 01_bronze_ingest.ipynb
│ ├─ 02_silver_transform.ipynb
│ └─ 03_gold_analytics.ipynb
├─ README.md
└─ LICENSE
```



---

## 📊 Data Sources

- **Population Dataset**  
  Source: https://github.com/datasets/population  
  Fields: `Country Name`, `Country Code`, `Year`, `Population`

- **CO₂ Emissions Dataset**  
  Source: https://github.com/owid/co2-data  
  Fields: `Country`, `Year`, `CO₂`, `CO₂ per capita`


---

## 📐 Output (Gold Layer)

The final dataset includes:

- Country  
- Year  
- Population  
- Total CO₂ emissions  
- CO₂ per capita  
- **CO₂ per 1,000 people**

This table is suitable for:
- BI dashboards  
- Semantic models  
- Time-series and cross-country analysis  

---

## 📄 License

This project is licensed and owned by **Jihad Hasan**  
GitHub: `jihadhasan210`


