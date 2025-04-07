# salary-prediction
Exploring which features impact salary most using regression, SHAP, and K-Means Clustering

# Salary Prediction Modeling

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Jacinda-Chen/salary-prediction/blob/main/salary_modeling.ipynb)

This project explores which features most influence salary using real-world data and a combination of linear and non-linear models. The notebook walks through data cleaning, exploratory analysis, multiple regression techniques, and SHAP for explainability.

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
- Used K-Means clustering to see how the data naturally groups
- Analyzed potential fairness issues, including gender impact on predictions

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

- Education level had the strongest linear influence on salary
- Age and years of experience dominated in the tree-based Random Forest model
- SHAP revealed which features drove individual predictions
- Gender had a small but measurable effect — showing the importance of fairness analysis
- Individuals with higher education and experience clustered into higher salary groups, consistent with model predictions.

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
