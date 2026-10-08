
# U.S. County Obesity and Diabetes Analysis

## Project Overview

This project investigates the relationship between obesity prevalence and diagnosed diabetes prevalence across U.S. counties using publicly available healthcare data from the Centers for Disease Control and Prevention (CDC).

The project uses R for statistical analysis, R Markdown for reproducible reporting, and public web APIs for accessing healthcare data.

## Research Question

**Is there a statistically significant relationship between obesity prevalence and diagnosed diabetes prevalence across U.S. counties?**

## Dataset

**Source:** CDC PLACES: Local Data for Better Health, County Data, 2024 Release

**Dataset URL:** https://data.cdc.gov/d/fu4u-a9bh

The analysis focuses on:

- Year: 2022
- Geographic level: U.S. counties and county-level geographic observations
- Obesity: Age-adjusted prevalence (%)
- Diagnosed diabetes: Age-adjusted prevalence (%)
- Sample size: 3,145 matched geographic observations

The original dataset includes county-level estimates for multiple health indicators. The analysis selects obesity and diagnosed diabetes prevalence and combines them by geographic identifier.

## Tools and Technologies

- R and RStudio
- R Markdown
- GitHub and GitHub Pages
- CDC PLACES Web API
- JSON
- curl and jq

## Statistical Analysis

The project includes:

1. Descriptive statistics for obesity and diabetes prevalence.
2. Scatterplots and linear regression analysis.
3. Pearson correlation testing.
4. A histogram of diabetes prevalence.
5. A comparison of lower-obesity and higher-obesity counties using the Wilcoxon rank-sum test.

## Key Findings

| Statistic | Result |
|---|---|
| Mean obesity prevalence | 37.91% |
| Mean diabetes prevalence | 11.13% |
| Pearson correlation coefficient | 0.7009 |
| Linear regression R-squared | 0.4913 |
| Wilcoxon rank-sum test p-value | < 0.001 |

The results indicate a strong positive association between obesity and diagnosed diabetes prevalence across U.S. counties.

The analysis is observational and uses aggregate geographic data, so the findings do not establish causation.

## Web API Exploration

The CDC PLACES API is used to retrieve:

- Obesity prevalence estimates for Georgia counties.
- Diabetes prevalence estimates for Georgia counties.
- Both obesity and diabetes prevalence estimates for Gwinnett County, Georgia.

## Project Files

This repository will contain:

- `CDC_dataset.csv` — Original CDC PLACES dataset.
- `OD_Markdown.Rmd` — R Markdown analysis source.
- `OD_Markdown.html` — Knitted HTML analysis report.
- `county_health_data.json` — JSON dataset for API queries.
- `README.md` — Project documentation.

## Data Source and Attribution

Centers for Disease Control and Prevention (CDC).

PLACES: Local Data for Better Health, County Data, 2024 Release.

https://data.cdc.gov/d/fu4u-a9bh

## Limitations

This analysis uses county-level prevalence estimates rather than individual patient records. Factors such as socioeconomic conditions, healthcare access, and physical activity may affect the observed relationship.

The results describe statistical associations and should not be interpreted as evidence of causation.
