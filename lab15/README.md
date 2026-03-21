# Forecasting Architecture and the Bias-Variance Tradeoff

## Objective
This project examines the bias-variance tradeoff in predictive modeling using NVIDIA quarterly revenue data. The goal is to understand how increasing model complexity affects model fit and out-of-sample performance.

## Methodology
- Built a linear regression model as a baseline to illustrate underfitting (high bias)
- Expanded the model using a 7th-degree polynomial to capture nonlinear patterns
- Evaluated model performance using training Mean Squared Error (MSE)
- Conducted extrapolation to test how the model behaves on unseen data
- Applied K-Fold Cross Validation to estimate out-of-sample error
- Implemented Ridge regression to reduce overfitting through regularization

## Key Findings
- The linear model fails to capture the nonlinear growth trend in the data
- The polynomial model fits the training data almost perfectly but shows clear signs of overfitting
- Predictions outside the sample become unstable and unrealistic
- Cross-validation reveals that the model performs poorly on unseen data
- Ridge regression produces a smoother and more stable fit by reducing variance
