# Seasonal Agriculture Performance Analysis

A Data Analytics major project (VOIS AICTE Batch 2026-2027) analyzing how agricultural
performance — yield, resource usage, and profitability — varies across seasons using a
real farm-level dataset.

## Problem Statement

Agricultural activities are influenced by seasonal variations in environmental
conditions, farming practices, resource availability, and market conditions. Raw
agricultural data does not clearly explain how performance changes across seasons or
what patterns can be observed under different seasonal conditions.

This project analyzes the given agricultural dataset to investigate seasonal
differences in agricultural performance by identifying meaningful patterns, trends,
relationships, and variations within the available data.

## Dataset

| | |
|---|---|
| Records | 4,000 farm-level entries |
| Seasons | Kharif, Rabi, Zaid |
| States | 8 |
| Districts | 10 |
| Crops | 8 (Wheat, Rice, Maize, Cotton, Pulses, Chilli, Groundnut, Sugarcane) |
| Columns | 28 (environmental, resource, and economic variables) |

Key variables include `Yield_Tonnes_Ha`, `Production_Tonnes`, `Rainfall_mm`,
`Avg_Temperature_C`, `Humidity_pct`, `Water_Used_m3`, `Water_Efficiency_t_per_1000m3`,
`Fertilizer_kg_ha`, `Total_Cost_INR`, `Revenue_INR`, and `Profit_INR`.

File: [`seasonal_agriculture_performance_dataset.csv`](./seasonal_agriculture_performance_dataset.csv)

## Objective

- Explore and understand the dataset
- Clean and prepare the data for analysis
- Examine how agricultural performance varies across seasons
- Identify important seasonal patterns and trends
- Investigate relationships between seasonal conditions and agricultural outcomes
- Compare relevant groups (crop, state, irrigation method) within seasons
- Apply appropriate statistical and visualization techniques
- Develop evidence-based conclusions and recommendations

## Tech Stack

- **Python** (Google Colab)
- **pandas, numpy** — data cleaning and manipulation
- **matplotlib, seaborn** — visualization
- **scipy.stats** — statistical hypothesis testing (Shapiro-Wilk, Levene's, Kruskal-Wallis)

## Project Workflow

1. Dataset loading and initial inspection
2. Data cleaning (missing values, duplicates)
3. Descriptive/statistical analysis and outlier investigation
4. Univariate, bivariate, and multivariate analysis
5. Correlation analysis
6. Seasonal comparisons
7. Three student-designed analyses:
   - Seasonal Resource Efficiency
   - Crop Performance Across Seasons
   - Yield and Profitability Relationship
8. Statistical hypothesis testing (Kruskal-Wallis)
9. Evidence-based insights, recommendations, limitations, and conclusion

## Key Findings

- **Kharif season leads** in both average yield (5.64 Tonnes/Ha) and average profit
  (₹178,914.65). **Zaid season is weakest**, with the lowest yield, highest water usage,
  lowest water efficiency, and a negative average profit (₹-24,804.82). This seasonal
  difference is statistically significant (Kruskal-Wallis test, p < 0.05).
- **Sugarcane dominates** yield (46.94 T/Ha) and profit (₹817,187.99) among all crops,
  while **Wheat, Rice, and Maize show negative average profit** despite reasonable
  yields — yield alone does not guarantee profitability.
- Individual environmental factors (rainfall, temperature, humidity, sunlight) show
  **almost no linear correlation** with yield (all between -0.015 and 0.031).
- **Water efficiency** correlates far more strongly with yield (0.915) than raw water
  volume used (0.389), suggesting *how* resources are used matters more than *how
  much* is used.
- **Punjab** has the highest average yield and profit among states; **Andhra Pradesh**
  the lowest yield.

*(Full list of 10 documented insights is in the notebook.)*

## Important Note on Causation

All relationships explored in this project are based on observational data. Findings
represent **associations**, not proof of cause and effect. Recommendations should be
validated further before real-world application.

## Repository Structure

```
├── README.md
├── seasonal_agriculture_performance_dataset.csv
├── Seasonal_Agriculture_Performance_Analysis.ipynb
├── Seasonal_Agriculture_Performance_Analysis.pptx
├── requirements.txt
└── images/
    ├── seasonal_yield_profit.png
    ├── crop_season_heatmap.png
    ├── correlation_heatmap.png
    └── water_efficiency.png
```

## How to Run

1. Clone this repository:
   ```
   git clone https://github.com/<your-username>/seasonal-agriculture-performance-analysis.git
   ```
2. Open `Seasonal_Agriculture_Performance_Analysis.ipynb` in
   [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
3. Install dependencies (already available by default in Colab):
   ```
   pip install -r requirements.txt
   ```
4. Upload `seasonal_agriculture_performance_dataset.csv` when prompted (or place it in
   the same directory if running locally), then run all cells in order.

## Limitations

- Single-season snapshot — no multi-year trend data available
- Limited to 8 states and 10 districts
- Observational data only — no controlled experiment, so causation cannot be established
- A small number of missing values (Rainfall_mm, Soil_Moisture_pct, Yield_Tonnes_Ha)
  were median-imputed during cleaning

## Author

**Chillarige Sai Dedeepya**
AICTE Student ID: STU6a6cb0045f0c31785507844
VOIS AICTE Batch 2026-2027 — Major Project



This project is submitted for academic purposes as part of the VOIS AICTE program.
