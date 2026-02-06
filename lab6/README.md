# Lab 6: The Architecture of Bias  
**Sampling Theory, Stratification, and SRM Forensics**

---

## Project Overview
This project studies how **bias originates from the Data Generating Process (DGP)** rather than from machine learning models themselves.  
Using the Titanic dataset as a controlled environment, I demonstrate how naïve random sampling can introduce systematic errors, and how these errors can be detected and corrected using statistical and engineering tools.

---

## Objective
The goal of this lab is to show that:

- Simple Random Sampling (SRS) can generate **sampling error and bias** in small datasets  
- Bias can exist **before any model is trained**  
- Correcting bias requires fixing the **data generation and sampling process**, not just improving models  

---

## Tech Stack
- Python  
- pandas, numpy  
- scipy (Chi-Square tests)  
- scikit-learn (Stratified Sampling)

---

## Methodology

### 1. Manual Simulation of Sampling Error
I manually implemented Simple Random Sampling by shuffling indices and performing an 80/20 split on the Titanic dataset.  
By comparing survival rates across training and test sets, I showed that even random splits can produce large deviations due to finite-sample variance.

**Key Insight:**  
Sampling error is not noise — it is structure revealed by small samples.

---

### 2. Fixing Covariate Shift with Stratified Sampling
Passenger class (`pclass`) was identified as a key covariate driving survival outcomes.  
Using stratified sampling (`train_test_split` with `stratify=pclass`), I enforced identical class distributions across training and test sets.

This eliminated covariate shift and stabilized survival rate estimates.

**Lesson:**  
Bias is usually a data problem, not a model problem.

---

### 3. SRM (Sample Ratio Mismatch) Forensic Diagnostic
To simulate real-world experimentation failures, I implemented a **Chi-Square SRM diagnostic** to test whether observed group proportions deviated from planned experimental splits.

This method is commonly used in A/B testing to detect:
- Load balancing errors  
- Logging or instrumentation bugs  
- Silent data loss in production pipelines  

---

## Theoretical Extension: Ghost Data & Heckman Selection Bias

### Why analyzing only successful startups creates bias
Platforms such as TechCrunch observe only **successful startups** (e.g., unicorns).  
Failed startups are rarely recorded, even though they are crucial for causal inference.

This creates **selection bias**, because:
- Survival is not random  
- Observed outcomes are conditional on success  
- Estimated relationships are systematically distorted  

The missing observations are referred to as **“Ghost Data.”**

---

### What type of Ghost Data is missing?
The missing data includes:
- Startups that failed before raising late-stage funding  
- Firms that exited early and never became publicly visible  
- Comparable startups rejected by investors  

This data is **not missing at random**.

---

### How Heckman Correction addresses this problem
The Heckman Selection Model explicitly models:
1. The **selection process** (probability of being observed)  
2. The **outcome process** (performance conditional on selection)  

By estimating the selection mechanism, Heckman correction adjusts for bias caused by missing ghost observations and enables valid inference despite incomplete data.

---

## Key Takeaways
- Randomness does not guarantee representativeness  
- Bias often originates upstream in data collection  
- Statistical diagnostics are essential for trustworthy ML systems  
- Ghost data must be modeled, not ignored  

---
