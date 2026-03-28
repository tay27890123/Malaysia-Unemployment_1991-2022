# Malaysia Unemployment Analysis (1991–2022)

End-to-end data analysis project exploring Malaysia's unemployment trends, employment sector shifts, and the relationship with GDP.

## About the Project

This project analyses 30 years of employment and GDP data for Malaysia using a public Kaggle dataset (183 countries, 1991–2022). I built a clean data pipeline and performed EDA + economic analysis, with separate views for the full period and the most recent 10 years (2012–2022) to better understand post-GFC and COVID effects.

## Notebooks

- **01_data_ingestion.ipynb**  
  Data loading, validation, checksum, metadata creation, and saving clean processed files.

- **02_eda.ipynb**  
  Exploratory data analysis: trends, distributions, sector changes, correlation heatmap, and pre/post-COVID comparison (full 32 years + recent 10 years).

- **03_economic_analysis.ipynb**  
  Okun’s Law testing (with and without 1-year lag), regression analysis, ASEAN country comparison, and simple linear forecast for 2023–2025.

## Key Findings

- Okun’s Law holds in Malaysia: higher GDP growth is associated with lower unemployment (negative relationship, stronger with 1-year lag).
- Unemployment rate increased noticeably after COVID (from ~3.3% pre-COVID average to ~4.4% post-COVID).
- Services sector has been very stable (~60–62% of employment) and appears to be the main source of labour market resilience.
- Malaysia’s unemployment rate is among the lower ones in ASEAN (based on 2010–2022 average).

## Policy Notes

Based on the analysis, maintaining GDP growth above 5% annually would help keep unemployment low. Continued focus on the services sector and youth reskilling would support long-term stability.

## Tech Stack

- Python 3
- pandas, numpy
- matplotlib + seaborn
- scipy, scikit-learn

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
Run the notebooks in order: 01 → 02 → 03.
Dataset Source
Kaggle – Global Jobs, GDP and Unemployment Data (1991–2022)
https://www.kaggle.com/datasets/akshatsharma2/global-jobs-gdp-and-unemployment-data-19912022
Limitations & Next Steps

This dataset uses general unemployment rate (not youth-specific 15–24).
Next step: replace with official DOSM monthly youth unemployment data for more targeted analysis.