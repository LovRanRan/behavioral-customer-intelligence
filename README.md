# Behavioral Customer Intelligence: Segmentation & Churn Modeling

## 📌 Overview

This project builds an end-to-end customer behavioral intelligence system combining:

- RFM-based customer segmentation
- Time-aware churn prediction
- Model interpretability using SHAP

The objective is to identify high-value and at-risk customers and prioritize retention strategies.

---

## 🧠 Business Problem

E-commerce platforms must proactively detect customers likely to churn.

This project simulates a real-world retention pipeline using:

- Historical feature construction
- A 30-day forward-looking churn prediction window
- Strict prevention of data leakage

---

## 🔬 Methodology

### 1️⃣ Data Processing
- Aggregated 330K+ transactional records into customer-level RFM features.
- Engineered Recency, Frequency, Monetary indicators.

### 2️⃣ Customer Segmentation
- Applied K-Means clustering.
- Evaluated cluster quality using Silhouette Score and Davies–Bouldin Index.
- Derived interpretable personas: Champions, Loyal, At-Risk, Dormant.

### 3️⃣ Time-Aware Churn Modeling
- Defined temporal cutoff to eliminate data leakage.
- Constructed 30-day forward churn label.
- Trained XGBoost classifier (AUC = 0.72).

### 4️⃣ Model Interpretability
- Applied SHAP to quantify feature importance.
- Identified purchase frequency and recency as dominant churn drivers.

---

## 📊 Model Performance

- ROC-AUC: 0.72
- F1 Score (Churned Users): 0.80
- Recall (Churned Users): 86%

---

## 🛠 Tech Stack

- Python (pandas, NumPy)
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib

---

## 📎 Dataset

UCI Online Retail Dataset:
https://archive.ics.uci.edu/ml/datasets/Online+Retail

(Note: Raw dataset is not included in this repository.)