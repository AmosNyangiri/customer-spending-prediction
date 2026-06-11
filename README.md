# Analyzing Customer Spending Using Multiple Linear Regression

## Overview

This project analyzes customer spending behavior using Multiple Linear Regression (MLR). The study quantifies the relationship between customer demographic and financial characteristics — such as age, loyalty years and preferred spending category — and their spending scores on a scale of 1 to 100.

---

## Objectives

- Fit a Multiple Linear Regression model to a customer analytics dataset
- Perform diagnostic checking of the model's regression assumptions
- Evaluate the predictive performance of the model
- Predict customer spending scores

---

## Dataset

- **Source:** Kaggle — Customer Analytics Dataset
- **Size:** 200 rows × 10 columns
- **Split:** 80% training / 20% testing

**Features used:**

| Variable | Description |
|---|---|
| Spending Score (1–100) | Target variable — customer spending level |
| Age | Customer age |
| Age Group | Categorical age bracket |
| Gender | Male / Female |
| Annual Income | Annual income (USD) |
| Estimated Savings | Estimated savings amount |
| Credit Score | Customer credit score |
| Loyalty Years | Years as a customer |
| Preferred Category | Budget / Electronics / Fashion / Luxury |

---

## Methodology

1. **Data Pre-processing** — Missing value imputation, dummy encoding of categorical variables, standardization of continuous variables and outlier treatment
2. **Exploratory Data Analysis (EDA)** — Descriptive statistics, correlation heatmap, distribution plots, scatterplots and box plots
3. **Model Development** — OLS Multiple Linear Regression (full model and reduced model)
4. **Assumption Diagnostics:**
   - Linearity — Residuals vs Fitted plot
   - Normality — Q-Q plot and Shapiro-Wilk test
   - Homoscedasticity — Breusch-Pagan test (HC3 robust standard errors applied)
   - Independence — Durbin-Watson test
   - Multicollinearity — Variance Inflation Factor (VIF)
5. **Model Evaluation** — MAE, MSE and RMSE on the test set

---

## Key Results

| Metric | Model 1 (Full) | Model 2 (Reduced) |
|---|---|---|
| R-squared | 0.918 | 0.917 |
| Adjusted R-squared | 0.912 | 0.913 |
| MAE | 7.174 | 7.109 |
| RMSE | 8.880 | 8.842 |

- The reduced model explains **91.7%** of the variation in spending scores
- **Loyalty years**, **age group** and **preferred spending category** were statistically significant predictors
- **Gender**, **annual income** and **credit score** were not statistically significant

---

## Tools and Technologies

- **Language:** Python
- **Libraries:** pandas, NumPy, scikit-learn, statsmodels, matplotlib, seaborn

---

## Author

**Amos Nyangiri**  
BSc Statistics and Information Technology — The Co-operative University of Kenya  
📧 amosnyangiri360@gmail.com
