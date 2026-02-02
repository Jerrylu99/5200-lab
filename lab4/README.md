# Lab 4 – The Tech Economist Mindset  
**Manual Forensics vs. Algorithmic Anomaly Detection**

## Objective
This lab explores why the **average can be misleading in skewed, real-world data**.  
Using the California Housing dataset, we move from **manual statistical forensics**
to **machine-learning–based anomaly detection**, and finally to an AI-assisted
“Tech Economist” robustness analysis.

---

## Dataset
- **Source:** California Housing Dataset (scikit-learn)
- **Key Feature:** `MedHouseVal` is capped at 5.0 ($500k), creating a ceiling effect
- **Focus Variable:** `MedInc` (Median Income)

---

## Phase Overview

### Phase 1 – Data Inspection
- Loaded and inspected the California Housing dataset
- Visualized the distribution of house values
- Identified the artificial ceiling effect at $500k

---

### Phase 2 – Manual Statistical Forensics (No AI)
- Implemented the **Interquartile Range (IQR)** method manually
- Computed:
  - Q1, Q3
  - IQR
  - Tukey Fence (1.5 × IQR)
- Flagged univariate income outliers
- Visualized results using a boxplot

**Key Insight:**  
The mean is highly sensitive to extreme high-income districts, while the median
remains stable.

---

### Phase 3 – Algorithmic Anomaly Detection
- Applied **Isolation Forest** for multivariate anomaly detection
- Features used:
  - Median Income
  - House Age
  - Average Rooms
  - Average Bedrooms
  - Population
- Detected anomalies based on **relationships between variables**, not just magnitude

---

### Phase 4 – AI “Tech Economist” Analysis
- Split data into:
  - Core Market (Normal)
  - Anomalies (Outliers)
- Compared:
  - Mean vs. Median
  - Standard Deviation vs. MAD
- Visualized income distributions for both groups

**Conclusion:**  
Outliers form a distinct “tail market” with higher volatility and inequality,
confirming that averages alone are unreliable in skewed economic data.

---

## Key Takeaway
Modern data analysis requires:
- Robust statistics (Median, MAD)
- Multivariate anomaly detection
- AI-assisted interpretation

This reflects how real-world PropTech and marketplace analytics are performed today.

---

## Files
- `lab4.ipynb` – Complete analysis notebook
