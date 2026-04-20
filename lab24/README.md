# Causal ML Lab 24 — DML and Causal Forests for Policy Evaluation

## Objective
This project applies modern causal machine learning methods to estimate treatment effects and analyze heterogeneity in observational data. The lab focuses on Double Machine Learning (DML), sensitivity analysis, and Causal Forests.

## Project Summary
In this lab, I diagnosed and corrected a broken manual DML implementation that contained several estimation issues, including data leakage in cross-fitting, missing treatment residualization, and an incorrect instrumental-variable formula for the treatment effect estimator.

After correcting the implementation, I verified that the estimator successfully recovered the true Average Treatment Effect (ATE = 5.0) in a simulated data-generating process.

I then applied DML to estimate the causal effect of 401(k) eligibility on net financial assets using Random Forest nuisance models with 5-fold cross-fitting.

To evaluate robustness, I performed sensitivity analysis to assess the potential impact of omitted variable bias from unmeasured confounders.

Finally, I implemented a Causal Forest model to estimate Conditional Average Treatment Effects (CATEs) at the individual level and compared those results with subgroup DML estimates based on quartiles.

## Methodology
- Fixed errors in a manual Double Machine Learning estimator
- Used cross-fitting to reduce overfitting bias
- Estimated treatment effects using orthogonalized residuals
- Applied Random Forest models for nuisance function estimation
- Conducted robustness checks through sensitivity analysis
- Estimated heterogeneous treatment effects using Causal Forests
- Compared subgroup-level and individual-level heterogeneity methods

## Key Findings
- The corrected DML estimator recovered the true simulated ATE accurately
- 401(k) eligibility had a positive causal effect on household net financial assets
- Results were reasonably robust to moderate unobserved confounding
- Causal Forests provided more detailed heterogeneity estimates than subgroup DML
- Individual-level treatment effects revealed patterns not captured by quartile grouping

## Files Included
- `lab_24_causal_ml.ipynb` — Main notebook with all analysis
- `causal_ml.py` — Reusable helper functions
- `cate_histogram.png` — Distribution of estimated treatment effects
- `sensitivity_plot.png` — Robustness analysis figure
- `README.md` — Project documentation

## Conclusion
This project demonstrates how causal machine learning methods can improve policy evaluation by combining credible causal inference with flexible machine learning tools. Compared with traditional average-effect models, these methods provide stronger robustness and richer insights into treatment effect heterogeneity.
