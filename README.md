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


- ## Key Visual Insights

### Top 10 Countries by Total Emissions
<img width="491" height="441" alt="Screenshot 2026-02-03 193053" src="https://github.com/user-attachments/assets/d47505ad-9f96-40e2-b074-f0ca616b1a16" /> 

**Insight:** Emissions are highly concentrated. China, the U.S., and India account for over half of global CO₂ output, with a steep drop after the top three countries.

### Top Countries by Emissions Per Capita

<img width="458" height="418" alt="Screenshot 2026-02-03 193220" src="https://github.com/user-attachments/assets/2e59f3b9-da7e-4bcc-9cec-13d0fb9f8a9d" />

**Insight:** Per-capita emissions reveal a different picture; smaller or highly industrialized nations (e.g., Palau, Qatar) show disproportionately high emissions per person compared to larger countries.

### Population vs Total Emissions: linear
<img width="514" height="460" alt="Screenshot 2026-02-03 193243" src="https://github.com/user-attachments/assets/531c9694-0ca2-40a2-b6f8-8287b7ce2985" />

**Insight:** Without log scaling, extreme emitters dominate the chart, masking trends among smaller countries, demonstrating the importance of transformation in data analysis.

### Population vs Total Emissions: log scale
<img width="540" height="452" alt="Screenshot 2026-02-03 193305" src="https://github.com/user-attachments/assets/793e47a7-ccdf-47ef-b131-cfaa4f345887" />

**Insight:** On a logarithmic scale, emissions and population show a strong positive relationship, but outliers indicate economic structure and energy systems matter as much as population size.





## How to Run
```bash
pip install requests pandas beautifulsoup4 matplotlib
python [final_projectPFE2.ipynb](https://github.com/user-attachments/files/25041876/final_projectPFE2.ipynb)
