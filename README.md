# Telco Churn Analysis (SQL-First)

## Overview
This repository showcases a **SQL-first data analysis workflow** applied to a Telco Customer Churn dataset.

The project is structured to simulate a real-world analytics environment where **SQL** is the primary tool for:
- data loading into a relational store (SQLite)
- data cleaning and standardization
- exploratory data analysis (EDA)
- advanced churn and revenue impact analysis

Python is used for orchestration within Jupyter and for visualizations.

---

## Objectives
- Load a CSV dataset into a relational database (**SQLite**) inside Jupyter
- Perform data understanding and data quality checks (nulls, duplicates, inconsistent values)
- Create a cleaned, analysis-ready table using **SQL transformations**
- Analyze churn patterns and business drivers (contract, tenure, services, satisfaction)
- Quantify churn impact (revenue and CLTV)
- Provide reusable SQL templates that can be adapted to similar datasets

---

## Project Structure
telco-churn-sql-analysis/
│
├── notebooks/
│ └── telco_sql_analysis.ipynb
│
├── data/
│ └── telco.csv
│
└── README.md

---

## Dataset
- The dataset is stored in `data/telco.csv`.
- The notebook expects a relative path from the notebook directory:
  - `../data/telco.csv`

If you move files around, update the `CSV_PATH` variable in the notebook.

---

## Key Analyses Included
- **Baseline KPIs:** overall churn rate, average revenue, satisfaction metrics
- **Segmentation (EDA):**
  - churn rate by contract type
  - churn rate by tenure buckets
  - churn rate by internet service/type
  - satisfaction vs churn comparison
- **Advanced analysis:**
  - Top-N churn categories and reasons
  - churn trend by quarter
  - CLTV and revenue comparisons between churned vs retained customers
  - outlier detection on monthly charges (IQR rule)
  - correlation between churn score and churn label (Pearson, computed via SQL aggregates)

---

## Technologies
- **SQL / SQLite**
- **Python**: pandas, matplotlib
- **Jupyter Notebook**

---

## How to Run
1) Clone the repository:
```bash
git clone https://github.com/Younesghz1993/telco-churn-sql-analysis.git
cd telco-churn-sql-analysis
