# bank-goodcredit-risk-prediction
End-to-end Credit Risk Prediction System using WOE, Logistic Regression, XGBoost and Stacking Ensemble.
# Bank GoodCredit – Credit Risk Prediction System

##  Project Overview

This project develops an **end-to-end Credit Risk Prediction system** for **Bank GoodCredit** to identify customers who are likely to default on their credit card payments.

The model analyzes **customer account history, enquiry behavior, and demographic attributes** to predict creditworthiness and help the bank **reduce financial risk and improve lending decisions**.

The solution implements **traditional credit risk modeling techniques (WOE + Logistic Regression)** along with **advanced machine learning models (XGBoost and Stacking Ensemble)** to achieve strong predictive performance.

---

#  Business Objective

Banks face significant financial losses due to **credit default risk**.
The objective of this project is to build a predictive system that can:

• Identify **high-risk customers**
• Improve **credit approval decisions**
• Reduce **loan default probability**
• Enable **risk-based customer segmentation**

### Target Variable

| Label | Description                                             |
| ----- | ------------------------------------------------------- |
| 0     | Customer has **Good Credit History**                    |
| 1     | Customer has **Bad Credit History (30+ Days Past Due)** |

---

#  Dataset Description

The dataset consists of anonymized banking data collected from three different sources:

### 1️) Customer Account Data

Contains historical account and payment information.

Examples:

* credit limit
* current balance
* past due amount
* interest rate
* payment history

### 2️) Customer Enquiry Data

Tracks customer credit enquiries.

Examples:

* enquiry amount
* enquiry purpose
* enquiry date

### 3️) Customer Demographics

Contains anonymized customer profile information.

Total Features after engineering: **66+**

Due to privacy policies, feature names were anonymized.

---

#  Machine Learning Pipeline

The project follows a **complete industry-standard ML workflow**.

```
Data Extraction
        ↓
Data Cleaning
        ↓
Feature Engineering
        ↓
WOE Binning
        ↓
Information Value Feature Selection
        ↓
Handling Class Imbalance (SMOTE)
        ↓
Model Training
        ↓
Hyperparameter Tuning
        ↓
Stacking Ensemble
        ↓
Model Evaluation
```

---

#  Feature Engineering

Important engineered features include:

• Average payment duration
• Days since last enquiry
• Mean enquiry amount
• Credit utilization ratios
• Payment behaviour indicators

These features help capture **customer financial behaviour patterns**.

---

#  Feature Selection

Feature importance was evaluated using **Information Value (IV)**.

Feature selection rule:

```
IV > 0.02
```

WOE transformation was applied to improve **model interpretability and stability**, which is commonly used in **credit scorecard modeling**.

---

#  Handling Imbalanced Data

The dataset had class imbalance.

To address this:

**SMOTE (Synthetic Minority Oversampling Technique)** was applied to balance the training dataset and improve model performance on minority class predictions.

---

#  Models Implemented

## 1️) Logistic Regression

Baseline model commonly used in **credit scoring systems**.

Advantages:

* interpretable
* stable
* widely accepted in banking

---

## 2️) XGBoost

Gradient Boosting model used to capture **non-linear relationships**.

Key benefits:

* strong predictive power
* handles complex feature interactions
* robust to overfitting

---

## 3️) Hybrid Stacking Ensemble Model

A **stacked ensemble model** was built combining:

* Logistic Regression
* XGBoost

Meta-model:

* Logistic Regression

Stacking improves prediction performance by **combining strengths of multiple models**.

---

#  Model Evaluation

Performance was evaluated using:

• ROC-AUC Score
• Gini Coefficient
• Confusion Matrix
• Classification Report
• Rank Ordering (Decile Analysis)

### Benchmark

Industry benchmark Gini score: **37.9**

The stacked model achieved improved predictive performance.

---

#  Rank Ordering (Decile Analysis)

Customers were segmented into **10 deciles based on predicted risk**.

Higher deciles represent **customers with higher probability of default**.

This helps banks:

* identify risky customers
* prioritize credit monitoring
* adjust lending strategies

---

#  Technologies Used

| Technology           | Purpose                      |
| -------------------- | ---------------------------- |
| Python               | Programming Language         |
| Pandas               | Data Manipulation            |
| NumPy                | Numerical Computing          |
| Scikit-Learn         | Machine Learning Models      |
| XGBoost              | Gradient Boosting Model      |
| ScorecardPy          | WOE Binning & IV Calculation |
| SMOTE                | Handling Imbalanced Data     |
| MySQL                | Data Extraction              |
| Matplotlib / Seaborn | Data Visualization           |
| Joblib               | Model Serialization          |


#  Business Impact

The developed system enables Bank GoodCredit to:

*   Predict customer credit default risk
*  Improve credit approval decision making
*  Reduce financial losses from bad loans
*  Build a scalable **credit scoring system**



#  Future Improvements

Possible enhancements:

• Deploy model using **FastAPI**
• Build **Streamlit dashboard for credit risk prediction**
• Add **SHAP explainability for model interpretability**
• Create **real-time credit scoring API**




**Prachi Patel**

Aspiring Data Scientist
Focused on Machine Learning, AI, and Risk Analytics


