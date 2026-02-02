# China Economic Dashboard (lab3 World Bank Data)

## Overview
This project corresponds to Lab 3 and focuses on building an executive economic dashboard using World Bank data.

This project pulls macroeconomic indicators from the World Bank API and constructs a **2×3 executive economic dashboard for China**.

While Guatemala was used as an illustrative example in lecture, this project applies the same analytical framework to **China** in order to demonstrate how the methodology generalizes to a different international context.

---

## Data Source
World Bank World Development Indicators (WDI), accessed via the `wbdata / wbapi` interface.

---

## Indicators Used
The following macroeconomic indicators are used to summarize China’s economic conditions:

- **GDP_Const** – Real GDP (constant prices)  
- **Inflation_CPI** – Inflation, consumer prices  
- **Unemployment_Rate** – Unemployment rate  
- **Tax_Rev_GDP** – Tax revenue (% of GDP)  
- **Gov_Exp_GDP** – Government expenditure (% of GDP)  
- **Exports_GDP** – Exports of goods and services (% of GDP)  
- **Imports_GDP** – Imports of goods and services (% of GDP)  
- **Gross_Dom_Savings** – Gross domestic savings (% of GDP)  
- **Gross_Cap_Formation** – Gross capital formation (% of GDP)

---

## Dashboard Structure
A **2×3 executive dashboard** is constructed using Matplotlib and Seaborn:

1. **Top Left:** Real GDP (line chart)  
2. **Top Middle:** Inflation rate (bar chart with zero reference line)  
3. **Top Right:** Unemployment rate (line chart)  
4. **Bottom Left:** Fiscal balance (tax revenue vs government spending, filled area)  
5. **Bottom Middle:** Trade balance (exports vs imports, filled area)  
6. **Bottom Right:** Savings vs investment (dual-line chart)

All visualizations use a dark background theme and are designed to emphasize comparative economic structure rather than raw growth alone.

---

## Notes on Country Selection
China was selected as the country of analysis for this assignment.  
All indicators, visualization techniques, and benchmarking logic follow the assignment instructions exactly; only the country of focus differs from the lecture example.

---

## Files
- `lab3.ipynb` – Main analysis notebook  
- `README.md` – Project documentation
