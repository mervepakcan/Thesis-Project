# Interpretable Machine Learning for Urban Housing Affordability

## Project Overview

This repository contains my Master's thesis project, completed at the **National University of Science and Technology POLITEHNICA Bucharest, Faculty of Automatic Control and Computers**.

**Thesis title:** *Interpretable Machine Learning for Urban Housing Affordability: A Data-Driven Analysis of U.S. Metropolitan Markets*
**Student:** Merve Pakcan
**Advisor:** Prof. dr. ing. Monica Drăgoicea
**Year:** 2026

The main objective of this research is to identify the most significant variables affecting housing price variation across U.S. metropolitan markets, with a focus on affordability, rental pressure, and market competitiveness. The project integrates visual analytics and interpretable tree-based machine learning to support both accurate prediction and a clearer understanding of housing market dynamics.

The study is framed within the context of sustainable urban development, particularly **SDG 11: Sustainable Cities and Communities**.

---

## Approach

- **Literature review:** A PRISMA systematic review of the sustainability literature, complemented by a focused review of urban housing and machine learning literature.
- **Data:** Seven Zillow Research datasets covering U.S. Metropolitan Statistical Areas (March 2018 – February 2025) were merged and cleaned into a final dataset of **9,893 observations**.
- **Exploratory analysis:** Distribution, correlation, and temporal/regional analysis using Python and SAS Visual Analytics.
- **Modeling:** Linear Regression was used for a preliminary comparison; the main analysis focused on three tree-based models — Decision Tree, Random Forest, and Gradient Boosting — each trained with default and tuned configurations in SAS Viya (Model Studio).
- **Interpretability:** Variable importance, icicle plots, node rules, and HyperSHAP local explanations to identify and explain the main drivers of median sale price.

The cleaned dataset (`merged_cleaned.csv`) and the Python notebook used to produce it (`Data_Prep_Cleaning_EDA.ipynb`) are available in this repository.

---

## Research Focus

1. What are the primary drivers of housing price variation across U.S. metropolitan regions, and how do affordability and market competitiveness indicators influence housing sale prices?
2. To what extent can tree-based machine learning models outperform traditional linear approaches in predicting urban housing prices?
3. How do housing prices and affordability metrics evolve temporally across U.S. regions between 2018 and 2025?
4. What interpretable and meaningful patterns can be extracted from tree-based models through visual analytics and rule-based interpretation?

---

## Models and Results

| Model | Configuration | Test RMSE ($) | Test R² |
|---|---|---:|---:|
| Decision Tree | Default | 48,339 | 0.918 |
| Decision Tree | Tuned | 38,999 | 0.947 |
| Random Forest | Default | 28,869 | 0.971 |
| Random Forest | Tuned | 33,918 | 0.960 |
| Gradient Boosting | Default | 29,616 | 0.969 |
| **Gradient Boosting** | **Tuned (Champion)** | **19,461** | **0.987** |

The tree-based ensemble models consistently outperformed the linear regression baseline. The tuned Gradient Boosting model achieved the strongest and most stable performance across all data partitions.

---

## Key Findings

- **Affordability drives price variation:** `YearsToSave` and `MedianRent` were consistently the strongest predictors; short-term market competitiveness indicators played a minor role.
- **Ensembles outperform linear and single-tree models:** The linear baseline showed heteroscedasticity, and the single decision tree underfit relative to the ensembles.
- **Temporal trends (2018–2025):** Prices and rents rose steadily, with the sharpest increase in 2021–2022.
- **Regional disparities:** California had the highest median sale price; Massachusetts and Wisconsin showed the strongest market competitiveness.
- **HyperSHAP explanations** confirmed affordability variables most often dominate individual predictions.

---

## Technologies Used

- **Python** — data integration, cleaning, and exploratory data analysis
- **SAS Viya** (Data Explorer, Visual Analytics, Model Studio) — modelling, tuning, and HyperSHAP interpretation
- **Zillow Research** — source of the housing market datasets

---

## Limitations

- All indicators come from a single source (Zillow) and cover U.S. metropolitan areas only.
- Other known price drivers (interest rates, household income, housing supply) were not included.
- Results reflect association, not causation.

See the full thesis for a detailed discussion of limitations and future research directions.
