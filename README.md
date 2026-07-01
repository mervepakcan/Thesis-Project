# Interpretable Machine Learning for Urban Housing Affordability

This repository contains my Master's thesis project, completed at the National University of Science and Technology POLITEHNICA Bucharest, Faculty of Automatic Control and Computer Science.

**Thesis title:**
*Interpretable Machine Learning for Urban Housing Affordability: A Data-Driven Analysis of U.S. Metropolitan Markets*

**Student:** Merve Pakcan
**Advisor:** Prof. Dr. Ing. Monica Drăgoicea
**Year:** 2026

---

## Overview

This thesis explores urban housing affordability in U.S. metropolitan markets using data analytics and interpretable machine learning.

The motivation behind the project comes from the growing pressure on housing affordability, especially in metropolitan areas where housing prices, rental costs, and regional differences have become long-term structural challenges. The study connects this topic with sustainable urban development, particularly SDG 11: Sustainable Cities and Communities.

The main goal of the project was not only to predict housing prices, but also to understand which factors explain price variation across regions and over time.

---

## Research Focus

The project investigates four main questions:

1. What are the main drivers of housing price variation across U.S. metropolitan regions?
2. Can tree-based machine learning models outperform a traditional linear regression baseline?
3. How did housing prices and affordability indicators evolve between 2018 and 2025?
4. What interpretable patterns can be extracted from machine learning models?

---

## Data and Methodology

The analysis is based on Zillow housing market indicators covering the period from 2018 to 2025 (9,893 observations across U.S. Metropolitan Statistical Areas).

The workflow included:

- data collection and integration from multiple Zillow datasets
- data cleaning and preprocessing
- exploratory housing market analysis
- feature engineering
- model development and evaluation (in SAS Viya / Model Studio)
- interpretation of model results (variable importance, node rules, HyperSHAP)

The main target variable was **Median Sale Price**.

The explanatory variables included affordability, rental pressure, market competitiveness, and supply-side indicators such as:

- Years To Save
- Median Rent
- Percentage Sold Above List
- Sale To List Ratio
- Market Heat Index
- New Construction Median Sale Price

---

## Models Used

Several models were developed and compared:

- Linear Regression (interpretable baseline)
- Decision Tree (default & tuned)
- Random Forest (default & tuned)
- Gradient Boosting (default & tuned)

The tree-based models were used because they can capture nonlinear relationships and interaction effects that are common in housing market data.

| Model | Configuration | Test RMSE ($) | Test R² |
|---|---|---:|---:|
| Decision Tree | Default | 48,339 | 0.918 |
| Decision Tree | Tuned | 38,999 | 0.947 |
| Random Forest | Default | 28,869 | 0.971 |
| Random Forest | Tuned | 33,918 | 0.960 |
| Gradient Boosting | Default | 29,616 | 0.969 |
| **Gradient Boosting** | **Tuned (Champion)** | **19,461** | **0.987** |

---

## Key Findings

The results showed that tree-based ensemble models performed better than the linear regression baseline.

The strongest model was the tuned Gradient Boosting model, which achieved the best predictive performance in the final evaluation (R² = 0.987).

Across the models, affordability-related variables were the most important drivers of housing prices. In particular, **Years To Save** and **Median Rent** had a strong influence on median sale prices, while short-term competitiveness indicators played a smaller role.

The findings suggest that interpretable machine learning can be useful not only for prediction, but also for understanding housing market structure and affordability dynamics.

---

## Repository Structure

The final thesis report and defense presentation are in the root folder. Earlier drafts and presentations from each semester (First, Second, Third) are available in the `Archive/` folder.

