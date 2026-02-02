## Deflating History with FRED: The Illusion of Growth & the Composition Effect

### Objective
Use FRED time-series data to compare nominal wages vs. inflation-adjusted real wages, and explain why the 2020 “wage spike” can be misleading.

### Data
- **AHETPI**: Average Hourly Earnings (nominal wage measure)
- **CPIAUCSL**: CPI (inflation measure)
- **ECIWAG**: Employment Cost Index (wage index designed to reduce composition bias)

### Method
1. Pulled wage and CPI series from FRED using the `fredapi` Python package.
2. Computed **Real Wage** by adjusting nominal wages using CPI (rebased to today’s prices).
3. Plotted **Nominal vs. Real** wages to show that nominal growth can exaggerate gains in purchasing power.
4. Addressed the 2020 “Pandemic Paradox” by comparing AHETPI to **ECIWAG** (ECI).  
   After rebasing both series (2015 = 100), AHETPI shows a sharper jump around 2020, while ECI is smoother—consistent with a **composition effect** in the average wage data.

### Key Takeaways
- Nominal wages rise strongly over the long run, but real wages are much flatter after adjusting for inflation.
- The 2020 spike in average hourly earnings is partly a statistical artifact: job losses were concentrated among lower-wage workers, which temporarily raised the average.
- The ECI-based series provides a more stable view of underlying wage growth during the pandemic period.
