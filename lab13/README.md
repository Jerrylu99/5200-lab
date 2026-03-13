# The Architecture of Dimensionality: Hedonic Pricing & the FWL Theorem

## Objective

This lab investigates how multivariate regression isolates the relationship between housing prices and structural attributes while controlling for confounding factors. Using a hedonic pricing framework, the analysis demonstrates the Frisch-Waugh-Lovell (FWL) theorem and its role in interpreting partial regression effects.

## Methodology

The analysis proceeds in several steps:

- Estimate a multivariate OLS regression predicting `Sale_Price` using `Property_Age` and `Distance_to_Tech_Hub`.
- Use the Frisch-Waugh-Lovell theorem to manually partial out the effect of the control variable.
- Verify that the coefficient from the residual regression matches the coefficient from the full multivariate regression.
- Extend the analysis with an interactive 3D visualization showing the fitted regression plane.

## Key Findings

The results demonstrate how omitted variable bias can distort interpretation in simple regressions. When proximity to technology hubs is omitted, the model falsely attributes higher prices to property age. Applying the FWL theorem isolates the independent variation in each predictor and recovers the correct partial effect.

The 3D visualization illustrates the regression hyperplane that represents predicted housing prices across combinations of property age and tech hub distance.
