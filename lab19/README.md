# Tree-Based Models and Model Interpretation (ECON 5200 Lab)

## Objective
This project applies tree-based machine learning models to a structured dataset and demonstrates the distinction between predictive performance and causal interpretation through model evaluation, hyperparameter tuning, and feature importance analysis.

---

## Methodology

- Compared three models:
  - Decision Tree Regressor
  - Ridge Regression
  - Random Forest Regressor

- Performed proper train-test split to evaluate out-of-sample performance

- Identified and corrected a model evaluation bug (training vs test set misuse)

- Tuned Random Forest hyperparameters using GridSearchCV:
  - n_estimators
  - max_depth
  - max_features

- Benchmarked tuned Random Forest against Gradient Boosting Regressor

- Analyzed feature importance using:
  - MDI (Mean Decrease in Impurity)
  - Permutation Importance
  - SHAP values

- Built reusable SHAP utilities for:
  - Local explanation (individual prediction)
  - Global explanation (feature importance)
  - MDI vs SHAP comparison

- Developed an interactive dashboard to:
  - Adjust model parameters
  - Visualize model performance
  - Compare feature importance methods

---

## Key Findings

- Random Forest outperformed Decision Tree and Ridge Regression in predictive accuracy on the test set.

- Hyperparameter tuning led to modest improvements, suggesting diminishing returns beyond a certain model complexity.

- Gradient Boosting performed competitively with Random Forest, with similar test R² values.

- MDI feature importance can be misleading due to bias toward features with more split opportunities.

- SHAP provided more stable and interpretable feature importance rankings.

- Importantly, feature importance measures reflect predictive relationships, not causal effects.

---

## Interpretation

This analysis highlights a central principle in machine learning:

> **Prediction does not imply causation.**

While tree-based models can effectively identify patterns and rank important features, they do not provide valid evidence for policy recommendations or causal claims without a proper identification strategy.

---

## Portfolio Value

This project demonstrates:

- Correct model evaluation practices
- Understanding of overfitting and data leakage
- Hyperparameter tuning and model comparison
- Advanced model interpretation using SHAP
- Ability to build reusable analytical tools
- Integration of modeling and visualization into an interactive workflow

---

## Tools

- Python (pandas, numpy, scikit-learn)
- SHAP for model interpretation
- matplotlib for visualization
- Streamlit for interactive dashboard

---

## Summary

Tree-based models provide strong predictive performance, but careful evaluation and interpretation are essential. This project emphasizes both technical modeling skills and the methodological discipline required to avoid incorrect causal conclusions.
