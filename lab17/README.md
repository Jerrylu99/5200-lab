# NY Fed Yield Curve Recession Prediction Model

## Project Overview  
This project replicates the Federal Reserve Bank of New York’s recession prediction model using logistic regression. The goal is to estimate the probability that the U.S. economy will enter a recession within the next 12 months based on the Treasury yield curve spread.

---

## Objective  
The main objective of this project is to understand how financial indicators can be used to predict macroeconomic outcomes. Specifically, the project aims to:
- Replicate a real-world recession forecasting model  
- Understand the limitations of linear probability models  
- Apply logistic regression for binary outcomes  
- Interpret model outputs such as probabilities and odds ratios  

---

## Data  
The data is obtained from the Federal Reserve Economic Data (FRED) database:
- **T10Y3M**: 10-year minus 3-month Treasury yield spread  
- **USREC**: NBER recession indicator  

The dataset spans from 1970 to the present and is processed into a monthly time series. The yield spread is lagged by 12 months to reflect forward-looking predictions.

---

## Methodology  
- Construct a logistic regression model using the lagged yield spread  
- Compare results with a linear probability model (OLS)  
- Estimate recession probabilities using `.predict_proba()`  
- Compute odds ratios and confidence intervals  
- Visualize predicted probabilities alongside historical recession periods  

---

## Key Findings  
- The yield curve is a strong leading indicator of recessions  
- Logistic regression produces valid probability estimates between 0 and 1  
- The model successfully captured increased recession risk prior to the 2008–2009 financial crisis  
- During the 2022–2024 inversion period, the model predicted elevated recession risk, although no recession occurred  

---

## Extension  
A second predictor, the unemployment rate (UNRATE), was added to the model:
- The extended model includes both financial and real economic indicators  
- Unemployment is positively associated with recession probability  
- The yield spread remains important but its effect decreases slightly  

---

## Conclusion  
This project demonstrates how logistic regression can be used to generate meaningful economic forecasts. While the yield curve is a strong predictor, combining it with additional macroeconomic variables provides a more comprehensive view of recession risk. Importantly, the model should be interpreted as probabilistic rather than deterministic.
