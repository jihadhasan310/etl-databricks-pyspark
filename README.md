# ETL Project: COVID-19 Analytics Pipeline

This project demonstrates a **complete ETL pipeline** built in **Databricks Community Edition** using **PySpark**. It is designed to be **GitHub-friendly** and showcase your data engineering skills.

## Project Overview

- **Objective:** Extract COVID-19 and population data from public internet sources, transform and clean it, and generate analytical tables.
- **Architecture:** Bronze / Silver / Gold (Medallion) pattern.
- **Technologies:** Databricks Community Edition, PySpark, Delta Lake.

## Repository Structure


```
etl-databricks-pyspark/
├─ notebooks/
│ ├─ 01_ingest_bronze.ipynb
│ ├─ 02_transform_silver.ipynb
│ └─ 03_analytics_gold.ipynb
├─ README.md
├─ requirements.txt # optional
└─ LICENSE
```



## Data Sources

- COVID-19 daily reports CSV: [Johns Hopkins GitHub](https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_daily_reports/01-01-2024.csv)
- Global population CSV: [Population dataset](https://raw.githubusercontent.com/datasets/population/master/data/population.csv)

## Execution Instructions

1. Open **Databricks Community Edition**.
2. Create a cluster (default runtime is sufficient).
3. Upload the notebooks in order:
   - `01_ingest_bronze.ipynb`
   - `02_transform_silver.ipynb`
   - `03_analytics_gold.ipynb`
4. Execute notebooks sequentially.
5. Explore results using SQL or Spark DataFrames.

## Notebook Descriptions

- **01_ingest_bronze.ipynb**: Reads data directly from public GitHub URLs and saves raw Delta tables (Bronze layer).
- **02_transform_silver.ipynb**: Cleans and transforms the data, saving Silver Delta tables.
- **03_analytics_gold.ipynb**: Joins datasets and computes analytical metrics, saving Gold Delta tables ready for BI or SQL analysis.

## Portfolio Highlights

- Uses **public datasets** for reproducibility.
- Modular notebook structure demonstrates **ETL skills with PySpark and Delta Lake**.
- Fully executable in **Databricks Community Edition**.
- Easy to extend for incremental loads, streaming, or dashboards.

## License

## License

This project is licensed by **Jihad Hasan (jihadhasan210)** under the MIT License.




