# High-Dimensional GDP Growth Forecasting with Regularized Regression

## Project Overview
This project examines the challenge of forecasting GDP per capita growth using a high-dimensional dataset of World Development Indicators (WDI). With a large number of predictors relative to observations, traditional OLS regression suffers from severe overfitting. To address this issue, I implement Ridge and Lasso regularization techniques to improve out-of-sample performance and identify the most informative predictors.

## Objective
- Forecast 5-year average GDP per capita growth across countries
- Demonstrate the limitations of OLS in high-dimensional settings
- Apply Ridge and Lasso regression with cross-validation
- Compare model performance and interpret feature selection results

## Data
- Source: World Bank World Development Indicators (WDI)
- Accessed via the `wbapi` Python package
- Includes ~35 development indicators across categories such as macroeconomics, education, infrastructure, health, and governance
- Time period: 2013–2019
- Cross-country dataset (~100–120 countries)

## Methodology
- Data preprocessing:
  - Averaged indicators over time
  - Dropped countries with excessive missing values
  - Imputed remaining missing values using cross-country medians
- Train-test split:
  - 70/30 split across countries
- Models:
  - OLS (baseline)
  - Ridge regression (with cross-validated lambda)
  - Lasso regression (with feature selection)
- Standardization:
  - Features scaled to zero mean and unit variance
- Evaluation metrics:
  - R² (train and test)
  - Mean Squared Error (MSE)

## Key Findings
- OLS exhibits severe overfitting, with high training R² but very poor test performance
- Ridge and Lasso significantly reduce overfitting and improve generalization
- Lasso selects a sparse subset of predictors, highlighting the most relevant variables
- Many predictors are highly correlated, leading to redundancy in high-dimensional settings
- Feature importance depends on the outcome variable, indicating context-specific economic relationships

## Conclusion
This project highlights the importance of regularization in high-dimensional economic modeling. While OLS fails due to overfitting, Ridge and Lasso provide more reliable predictions and better interpretability. The results also emphasize the difference between predictive relevance and economic significance, especially in datasets with strong multicollinearity.
