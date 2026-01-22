# Customer Churn Prediction (Telecom)

## Executive Summary
This project builds and evaluates machine learning models to predict customer churn using telecom customer data. The goal is to identify customers at high risk of leaving and provide actionable insights to support data-driven retention strategies.

---

## Problem Statement
Customer churn is a major business challenge for subscription-based services. Retaining existing customers is often more cost-effective than acquiring new ones. This project aims to predict which customers are likely to churn and identify the key factors driving churn behavior.

---

## Dataset
- Telco Customer Churn Dataset
- Includes customer demographics, contract details, services, billing information, and churn status

Target variable:
- **Churn** (Yes / No)

---

## Methodology
1. Data cleaning and preprocessing
2. Handling missing values and encoding categorical features
3. Train-test split with stratification
4. Model training:
   - Logistic Regression (baseline + class imbalance handling)
   - Random Forest (non-linear comparison model)
5. Model evaluation using ROC-AUC and recall
6. Feature interpretation and business analysis

---

## Model Selection
Although the Random Forest model captured non-linear interactions, Logistic Regression achieved higher ROC-AUC and better recall for churned customers. Since the primary business goal is to identify at-risk customers for retention efforts, recall and interpretability were prioritized. Logistic Regression was selected as the final model for churn risk scoring.

---

## Key Results
- Logistic Regression ROC-AUC: ~0.84
- Improved recall for churned customers using class-weighted training
- Strong churn drivers identified:
  - Month-to-month contracts
  - High monthly charges
  - Low customer tenure
  - Fiber optic service without support add-ons

---

## Business Action Plan
Customers on month-to-month contracts with high monthly charges and low tenure represent the highest churn risk segment. Retention strategies should prioritize this group through targeted incentives such as discounted long-term contracts, loyalty rewards, or enhanced onboarding support during the first few months of service.

---

## Tools & Technologies
- Python
- pandas, NumPy
- scikit-learn
- matplotlib

---

## Future Improvements
- Add gradient-boosted models (e.g., XGBoost)
- Deploy an interactive dashboard for churn risk monitoring
- Incorporate customer lifetime value into retention prioritization
