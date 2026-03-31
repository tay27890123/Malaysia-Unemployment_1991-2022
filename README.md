# Malaysia Unemployment Analysis (1991–2022)

End-to-end data analysis project exploring Malaysia's unemployment trends, employment sector shifts, and the relationship with GDP.

## About the Project

This project analyses 32 years of employment and GDP data for Malaysia using a public Kaggle dataset. I built a clean, reproducible data pipeline and performed both exploratory data analysis and economic analysis.

I analysed the data in two ways:
- Full period: 1991–2022 (32 years)
- Recent period: 2012–2022 (10 years) – to focus on more recent post-GFC and COVID dynamics

## Notebooks

- **01_data_ingestion.ipynb**: Data loading from raw CSV, validation, SHA-256 checksum, metadata creation, and saving clean processed files.
- **02_eda.ipynb**: Exploratory data analysis including time-series trends, histograms, boxplots, correlation heatmap, and employment sector changes. Separate analysis for full 32 years and recent 10 years.
- **03_economic_analysis.ipynb**: Economic modelling – tested Okun’s Law with linear regression (with and without 1-year time lag) which we call Time lag effect, also ASEAN 10-country comparison, and simple linear forecast for 2023–2025.

## Key Findings

- Unemployment rate increased noticeably after COVID (pre-COVID average ~3.3%, post-COVID ~4.4%).
- Services sector has remained very stable at ~60–62% of total employment and continues to be the main source of labour market resilience.
- Malaysia maintains one of the lower unemployment rates among ASEAN countries (2010–2022 average).

## Key Findings OKun's Law

- Okun’s Law direction is consistent with economic theory: higher GDP growth is associated with lower unemployment (negative relationship).
- However, the statistical relationship is relatively weak in this dataset:
  - Without lag: Slope = -0.002, R² = 0.002, p-value = 0.805 (not statistically significant)
  - With 1-year lag: Slope = -0.009, R² = 0.047, p-value = 0.248 (still not significant at 5% level)
- This suggests that other omitted factors (labour market policies, foreign worker inflows, global shocks, etc.) play a significant role in Malaysia’s unemployment dynamics.

## Policy Notes

The analysis suggests that:
- Sustained GDP growth above 5% per year would help keep unemployment low.
- Continued investment in the services sector and youth reskilling programmes would strengthen long-term labour market stability.
- Policymakers should pay close attention to external shocks, as the post-COVID period showed higher volatility.

## Tech Stack

- Python 3
- pandas, numpy
- matplotlib, seaborn
- scipy, scikit-learn

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
Run the notebooks in this order: 01 → 02 → 03.
Dataset
Kaggle – Global Jobs, GDP and Unemployment Data (1991–2022)
https://www.kaggle.com/datasets/akshatsharma2/global-jobs-gdp-and-unemployment-data-19912022

Limitations
This dataset uses general unemployment rate (not youth-specific 15–24 data).

Project 2.0 Concept 
 Replace with official DOSM monthly youth unemployment data for more targeted analysis.