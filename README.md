# Customer Churn Prediction

## Project Overview

Customer churn is one of the most important business challenges for subscription-based companies. Losing existing customers is often more expensive than acquiring new ones.

This project builds a complete Machine Learning pipeline to predict whether a customer is likely to churn based on demographic information, services, customer behavior, and account history.

The project follows an end-to-end Data Science workflow, including data cleaning, exploratory data analysis, feature engineering, model development, and evaluation.

---

# Business Problem

Customer retention has a significant impact on company revenue.

The objective of this project is to identify customers who are likely to leave the company so that the business can proactively apply retention strategies.

---

# Dataset

The dataset contains customer information including:

* Customer demographics
* Account information
* Internet services
* Phone services
* Billing information
* Customer satisfaction
* Contract details
* Churn status (Target)

Target Variable:

* `churn_label`

  * 1 → Customer Churned
  * 0 → Customer Stayed

---

# Project Workflow

## 1. Data Cleaning

* Removed duplicate records
* Checked missing values
* Verified data types
* Cleaned inconsistent values
* Exported a clean dataset

Notebook:

`03_data_cleaning.ipynb`

---

## 2. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand customer behavior.

Main analyses included:

* Target distribution
* Numerical feature analysis
* Categorical feature analysis
* Correlation analysis
* Business insights

Key findings:

* Satisfaction Score is strongly associated with churn.
* Month-to-Month contracts have the highest churn rate.
* Short-tenure customers churn more frequently.
* Fiber Optic customers have higher churn rates.
* Higher monthly charges are associated with increased churn.

Notebook:

`04_eda.ipynb`

---

## 3. Feature Engineering

Created new business-oriented features including:

* Average Revenue Per Month
* Contract Risk Score
* Referral Engagement Score

Several engineered features were evaluated and only meaningful ones were retained.

Notebook:

`05_feature_engineering.ipynb`

---

## 4. Modeling

Machine Learning models were trained and compared.

Models:

* Logistic Regression
* Logistic Regression (Balanced)
* Random Forest Classifier

The dataset was split using an 80/20 Train-Test Split.

StandardScaler was applied before Logistic Regression.

Notebook:

`06_modeling.ipynb`

---

## 5. Model Evaluation

Models were compared using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

Random Forest achieved the best overall performance.

---

# Final Model Performance

## Random Forest

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 96%   |
| Precision | 97%   |
| Recall    | 89%   |
| F1 Score  | 93%   |

Confusion Matrix:

```
[[1023   12]
 [  41  333]]
```

---

# Project Structure

```
Customer-Churn-Prediction/

│
├── data/
│
├── models/
│   ├── random_forest.pkl
│   └── scaler.pkl
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_data_cleaning.ipynb
│   ├── 04_eda.ipynb
│   ├── 05_feature_engineering.ipynb
│   ├── 06_modeling.ipynb
│   └── 07_evaluation.ipynb
│
├── reports/
│
├── src/
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

---

# Installation

Clone the repository

```bash
git clone https://github.com/your_username/customer-churn-prediction.git
```

Move into the project

```bash
cd customer-churn-prediction
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# Future Improvements (Version 2)

Planned improvements include:

* Hyperparameter Tuning
* Cross Validation
* Feature Selection
* XGBoost and LightGBM
* SHAP Explainability
* Model Deployment with Streamlit
* Docker Containerization
* CI/CD Pipeline
