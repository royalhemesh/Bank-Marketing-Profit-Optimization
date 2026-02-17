# A Data-Driven Solution to Inefficient Bank Marketing Campaigns

## Executive Summary

In a dataset of 41,188 bank customers, only ~11% subscribed to a term deposit.

Traditional marketing campaigns call every customer, resulting in high operational cost and low return.

This project replaces blanket calling with probability-driven targeting using machine learning and threshold optimization to maximize net profit.

The focus was not model accuracy alone — it was financial impact.

---

## Business Problem

- Conversion rate: ~11%
- Severe class imbalance
- High cost per outbound call
- Revenue generated only when a customer subscribes

Core Question:

Who should NOT be contacted in order to reduce waste while retaining most conversions?

---

## Dataset Overview

- 41,188 customer records
- Binary classification (Subscribed: Yes / No)
- Behavioral, demographic, and campaign interaction variables

### Class Distribution

![Class Distribution](images/class_distribution.png)

---

## Methodology

1. Data cleaning and preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature engineering
4. Model benchmarking:
   - Logistic Regression
   - Random Forest
   - Gradient Boosting
5. Cross-validation using ROC-AUC
6. Precision-Recall evaluation due to imbalance
7. Threshold optimization
8. Profit simulation based on:
   - Per-call operational cost
   - Revenue per successful conversion

---

## Model Performance

- Final Model: Gradient Boosting
- Cross-validated ROC-AUC: ~0.93
- Evaluated using ROC and Precision-Recall curves

### ROC Curve

![ROC Curve](images/roc_curve.png)

### Precision-Recall Curve

![Precision Recall Curve](images/pr_curve.png)

---

## Business Optimization

Using the default probability threshold (0.50) does not maximize profit.

Optimized decision threshold: ~0.35

This adjustment balances recall and cost efficiency.

### Profit vs Threshold

![Profit vs Threshold](images/profit_vs_threshold.png)

---

## Results at Optimized Threshold

- 40–45% fewer customers contacted
- Majority of actual subscribers retained (high recall)
- ~50%+ higher net profit compared to blanket calling at the same volume

---

## Key Insights

The most influential predictors were:

- Call duration
- Previous campaign outcome
- Contact timing

Demographic variables were less impactful than behavioral indicators.

### Feature Importance

![Feature Importance](images/feature_importance.png)

---
---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Strategic Takeaway

High-performing data science reduces operational waste before optimizing accuracy.

The true leverage of machine learning comes from aligning model decisions with financial outcomes rather than maximizing a single metric.
