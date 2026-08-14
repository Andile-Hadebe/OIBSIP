# 🛡️ Credit Card Fraud Detection with Machine Learning

## 📊 Project Overview

This project builds a machine learning model to detect fraudulent credit card transactions. The dataset contains **10,000 transactions** with only **1.51%** fraudulent cases — making this a severe class imbalance problem.

Completed as part of my Data Analytics internship at **Oasis Infobyte**.

## 🎯 Objectives

- Handle severe class imbalance (1.51% fraud)
- Build and compare fraud detection models
- Prioritize recall (catching fraud) over accuracy
- Provide business-relevant insights

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Core language |
| pandas | Data manipulation |
| numpy | Numerical operations |
| matplotlib | Static visualizations |
| seaborn | Statistical visualizations |
| scikit-learn | Modeling & evaluation |
| imbalanced-learn | SMOTE for oversampling |

## 📊 Key Findings

| Feature | Insight |
|---------|---------|
| **Amount** | Fraudulent transactions tend to be higher value |
| **Device Trust Score** | Lower scores are associated with fraud |
| **Location Mismatch** | Strong indicator of potential fraud |
| **Velocity** | Multiple transactions in 24h is a risk factor |

## 📈 Model Performance

| Model | Recall | Precision | F1 Score | AUC-ROC |
|-------|--------|-----------|----------|---------|
| **Logistic Regression** | 1.00 | 0.073 | 0.136 | 0.972 |
| **Random Forest** | 0.644 | 0.192 | 0.296 | 0.939 |

## ⚠️ Critical Lesson: Accuracy is Misleading

In imbalanced datasets, accuracy is dangerous. A model predicting "not fraud" for everything would achieve **98.49% accuracy** but catch **zero frauds**.

**Use these metrics instead:**
- **Recall** — How many actual frauds were caught?
- **Precision** — How many fraud alerts were correct?
- **F1 Score** — Harmonic mean of precision and recall
- **AUC-ROC** — How well does the model separate classes?

## 🚀 How to Run

1. Clone this repository
2. Ensure Python 3.x is installed
3. Install dependencies:
