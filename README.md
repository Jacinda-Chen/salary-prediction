# salary-prediction
Exploring which features impact salary most using regression, SHAP, and K-Means Clustering with PCA visualization. Performed a one-way ANOVA test and t-test to assess statistical significance. Interact with salary data on Tableau Public.

# Salary Prediction Modeling

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Jacinda-Chen/salary-prediction/blob/main/salary_modeling.ipynb)

This project explores which features most influence salary using real-world data and a combination of linear and non-linear models. The notebook walks through data cleaning, exploratory analysis, multiple regression techniques, SHAP for explainability, and k-means clustering.

---

## Project Overview

This project uses a real-world salary dataset from Kaggle to explore which features most influence salary predictions.
[View dataset here on Kaggle](https://www.kaggle.com/datasets/rkiattisak/salaly-prediction-for-beginer/data)

- Cleaned and preprocessed salary data (missing values, one-hot encoding, multicollinearity)
- Built predictive models:
  - Simple & Multiple Linear Regression
  - Ridge and Lasso Regression
  - Random Forest Regressor
- Used SHAP to explain model behavior and feature contributions
- Used K-Means clustering to see how the data naturally groups with PCA visualization
- Analyzed potential fairness issues, including gender impact on predictions and Welch's t-test for statistical significance

---

## Model Performance Summary

| Model                      | R² Score  | MAE      | RMSE     |
|----------------------------|-----------|----------|----------|
| Simple Linear Regression   | 0.899     | 12094.2  | 15551.0  |
| Multiple Linear Regression | 0.914     | 10042.0  | 14343.8  |
| Ridge Regression           | 0.915     | 9959.4   | 14237.2  |
| Lasso Regression           | 0.907     | 10284.7  | 14927.5  |
| Random Forest Regression   | 0.902     | 9610.7   | 15324.5  |

---

## Key Insights

- Education level had the strongest linear influence on salary (Average salary by education levels were statistically significant by a one-way ANOVA test)
- Age and years of experience dominated in the tree-based Random Forest model
- SHAP revealed which features drove individual predictions
- Gender had a small but measurable effect, but was not statistically significant according to Welch's t-test
- Individuals with higher education and experience clustered into higher salary groups, consistent with model predictions

---
## Interactive Dashboard

You can view the full Tableau dashboard here:

[Explore the Salary Dashboard on Tableau Public](https://public.tableau.com/views/SalaryPredictionandInsights/Salary?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## Project Structure

```
salary-prediction-project/
├── salary_modeling.ipynb # Main notebook
├── README.md # Project overview
├── requirements.txt # Dependencies
├── images/ # Visualizations (SHAP, charts)
├── data/ # sample CSV from Kaggle
└── .gitignore # Files to ignore
```
