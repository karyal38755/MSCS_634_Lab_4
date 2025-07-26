# Lab 4

### Purpose of This Lab
The goal of this lab was to explore core regression techniques; linear, multiple,
polynomial, Ridge, and Lasso; by applying them to the Diabetes dataset from 
`sklearn.datasets`. The lab was designed to build a conceptual and practical 
understanding of how different regression models behave, how regularization 
controls overfitting, and how evaluation metrics guide model selection. Each model 
was tested, visualized, and analyzed to understand both predictive performance and 
underlying data relationships.

### Findings

- **Simple Linear Regression** using a single feature (`bmi`) served as a baseline
  but showed clear limitations in capturing the complexity of disease progression.
- **Multiple Linear Regression** significantly improved performance by leveraging 
  all available features, increasing explained variance to over 50%.
- **Polynomial Regression** (degrees 2–3) captured non-linear interactions and 
  slightly improved results, but higher-degree models (e.g., degree 5) overfit the training data.
- **Ridge and Lasso Regression** were critical in demonstrating how regularization
  handles model complexity. Ridge offered stability, while Lasso provided feature 
  selection; dropping irrelevant features altogether.
- The **bias-variance tradeoff** was central: simple models underfit, complex ones
  overfit, and regularized models hit the sweet spot in between.

### Challenges & Decisions

- **Feature Selection for Simple Linear Regression**: BMI was chosen intentionally, 
  not arbitrarily, due to its known correlation with diabetes progression.
- **Polynomial Degree Choice**: Rather than blindly increasing the degree, degrees 
  2, 3, and 5 were selected to illustrate the progression from useful non-linearity 
  to overfitting.
- **Alpha Tuning**: Ridge and Lasso were tested on a wide range of alpha values. 
  We observed that high alpha penalized model complexity effectively, but risked underfitting.
- **Metric Interpretation**: Balancing between MAE, RMSE, and R² was crucial. R² 
  alone didn’t always reveal the whole story; especially in the presence of variance or outliers.
- **Visualization Design**: Plots were built not just to display results, but to 
  *show patterns*. Actual vs predicted scatter plots gave the clearest signal of model performance.

### Learnings
- No single regression model is best in all cases; **context and constraints matter**.
- Regularization isn’t optional when model complexity increases.
- Evaluation metrics are just numbers without thoughtful interpretation.
- Even clean datasets can lead to misleading conclusions if models aren’t carefully analyzed.

