# Global Purchasing Power Parity Analysis via the Big Mac Index

## Objective
This project empirically tests the **Law of One Price** using the Big Mac Index as a standardized consumption good. By comparing local Big Mac prices across countries, the analysis evaluates whether market exchange rates align with implied Purchasing Power Parity (PPP) relative to the US dollar.

## Data
The dataset is based on **The Economist’s Big Mac Index (January 2015)**.  
For the initial stage of the lab, the data were **manually constructed** using Python dictionaries, reinforcing understanding of data structures, variable types, and economic data organization.

## Methodology
- Manually created a country-level dataset containing ISO codes, local Big Mac prices, and market exchange rates.
- Converted local prices into USD using prevailing exchange rates.
- Calculated **implied PPP exchange rates** by benchmarking each country against the US Big Mac price.
- Computed the percentage **currency misalignment** (under- or overvaluation) relative to the US dollar.
- Visualized currency valuation using a horizontal bar chart to clearly illustrate deviations from fair value.

## Key Findings
The results reveal substantial cross-country variation in currency valuation. Several emerging market currencies appear significantly **undervalued** relative to the US dollar, while certain advanced economies—most notably Norway—exhibit evidence of **overvaluation**. These findings highlight persistent short-run deviations from Purchasing Power Parity and illustrate the usefulness of the Big Mac Index as an intuitive benchmark for exchange rate analysis.

## Tools
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn

