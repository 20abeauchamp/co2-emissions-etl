# co2-emissions-etl
End-to-end Python ETL pipeline that scrapes, cleans, stores, and analyzes global CO₂ emissions data using Pandas and SQL.

# Global CO₂ Emissions ETL & Analysis Pipeline

## Overview
This project builds an end-to-end data pipeline that:
1) Scrapes country-level CO₂ emissions data from a live website  
2) Cleans and normalizes messy web data (Unicode, symbols, numeric parsing)  
3) Stores structured data in a relational SQLite database  
4) Exports a cleaned dataset for reporting/analysis  
5) Generates descriptive statistics and visualizations

## Tech Stack
- Python (requests, BeautifulSoup, pandas)
- SQLite + SQL
- Matplotlib

## Pipeline Steps
- **Ingest:** scrape and parse HTML table data  
- **Transform:** clean text → numeric, handle missing values, standardize formatting  
- **Load:** write to SQLite with normalized tables (`countries`, `emissions`)  
- **Analyze:** descriptive stats (mean/median/variance/std)  
- **Visualize:** top emitters, per-capita comparisons, population vs emissions (linear + log)

## How to Run
```bash
pip install requests pandas beautifulsoup4 matplotlib
python [final_projectPFE2.ipynb](https://github.com/user-attachments/files/25041876/final_projectPFE2.ipynb)
