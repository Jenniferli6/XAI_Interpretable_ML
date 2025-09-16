# XAI Interpretable ML – Telco Customer Churn

## 🎯 Project Goal
The goal of this project is to **analyze customer churn in a telecommunications company** using interpretable machine learning models. By applying **Linear Regression, Logistic Regression, and Generalized Additive Models (GAMs)**, we aim to:
* Perform exploratory data analysis (EDA) to understand churn patterns
* Check model assumptions to ensure validity
* Build and interpret three different models
* Compare performance and interpretability
* Provide recommendations for reducing churn

## 📂 Project Structure

```
XAI_Interpretable_ML/
│── .gitignore               
│── README.md                 
│── Telco-Customer-Churn.csv    # Dataset from Kaggle
│── XAI_Interpretable_ML.ipynb  # Colab notebook with full workflow
```

## 📊 Dataset

We use the **Telco Customer Churn dataset** from Kaggle:
🔗 [Telco Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/code)

Example variables:

* Demographic: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* Account: `tenure`, `Contract`, `PaymentMethod`, `PaperlessBilling`
* Services: `PhoneService`, `InternetService`, `StreamingTV`, `TechSupport`
* Charges: `MonthlyCharges`, `TotalCharges`


## 📊 Workflow Summary
1. **Data Preparation & Cleaning**
   * Load dataset, check missing values, and adjust data types.
   * Remove non-predictive or redundant variables.
2. **Exploratory Data Analysis (EDA)**
   * Examine distributions, correlations, and feature relationships with churn.
   * Visualize numerical and categorical features.
3. **Assumption Checks**
   * Evaluate statistical and diagnostic tests for linear, logistic, and GAM models.
4. **Model Development**
   * Implement Linear Regression, Logistic Regression, and GAM.
   * Train/test split for evaluation.
5. **Model Comparison**
   * Assess predictive performance and interpretability.
   * Provide recommendations based on business goals.

## 📈 Model Performance

| Model              | Primary Metric(s)             | Test Performance                               |
|--------------------|-------------------------------|------------------------------------------------|
| Linear Regression  | MSE / R²                      | MSE: 0.1463<br>R²: 0.2501                      |
| Logistic Regression| Accuracy / AUC / F1 (weighted)| Accuracy: 79.96%<br>AUC: 0.831<br>F1: 0.79     |
| GAM                | Accuracy / AUC / F1 (weighted)| Accuracy: 79.60%<br>AUC: 0.839<br>F1: 0.79     |


## 📌 Recommendations for Telco Company

In this case, churn is fundamentally a binary classification problem.
* My primary recommendation is to use logistic regression because it offers an excellent balance: ~80% accuracy, strong AUC (0.831), and straightforward odds-ratio interpretations.
* My secondary suggestion would be GAM. The analysis reveals significant non-linear patterns, switching to GAM provides a ~1% AUC improvement. It's ideal for deeper insights, like tailoring offers based on tenure thresholds, but requires more expertise for deployment.
* I would not recommend using the Linear Regression model in this case due to its low R² and poor fit for binary outcome variables.







