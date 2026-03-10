# Predicting Customer Spending Behaviour in Streaming Services

> **Understanding AI Module | University of Hull**  
> Author: Muhammad Salahuddin

---

## 📌 Project Overview

This project applies **supervised and unsupervised machine learning** to a streaming service dataset to predict customer spending, classify churn risk, and segment customers into behavioural clusters.

The analysis covers the full ML pipeline: regression, classification, neural networks, and clustering — directly applicable to real-world subscription business intelligence.

---

## 🎯 Tasks Covered

- **(a–b)** Single and multi-variable regression to predict Monthly Spend
- **(c)** Regression with categorical variables using Random Forest
- **(d)** Artificial Neural Network (ANN) for spend prediction
- **(e)** Best model comparison and conclusions
- **(f)** Churn classification with Random Forest Classifier
- **(g–h)** Customer segmentation with K-Means and Hierarchical Clustering

---

## 📊 Results Summary

### Regression — Predicting Monthly Spend

| Model | R² Score |
|-------|----------|
| Single Feature (Satisfaction Score) | 0.546 |
| Polynomial Regression | 0.546 |
| **Multi-variable Linear Regression** ⭐ | **0.959** |
| Random Forest Regressor (with categoricals) | 0.933 |
| ANN (MLPRegressor) | 0.946 |

**Key Finding:** Multi-variable Linear Regression achieved the best R² of 0.959 — outperforming both Random Forest and the ANN. The Satisfaction Score was the strongest single predictor (R²=0.546), but multi-feature models revealed that Subscription Length and Support Tickets are equally important drivers of spend.

### Churn Classification — Random Forest Classifier

| Metric | Score |
|--------|-------|
| Accuracy | 1.00 |
| Precision | 1.00 |
| Recall | 1.00 |
| F1-Score | 1.00 |
| AUC-ROC | 1.00 |

> Perfect classification scores suggest strong feature separation in this dataset for churn prediction.

### Clustering — Customer Segmentation

| Algorithm | Optimal Clusters | Method Used |
|-----------|-----------------|-------------|
| K-Means | k=3 | Elbow method + PCA visualisation |
| Hierarchical | 3–4 | Dendrogram analysis |

**Cluster Profiles (K-Means, k=3):**
- Cluster 0: Central group — moderate spending and engagement
- Cluster 1: High-value outliers — elevated spend on key features
- Cluster 2: Low-engagement sparse group — churn risk segment

---

## 🔬 Methodology

### Data Preparation
- One-hot encoding for categorical variables (Gender, Region, Payment Method)
- StandardScaler normalisation for numerical features
- Missing value imputation
- 80/20 train-test split

### Models Implemented

**Regression:**
- Simple Linear Regression (per numerical feature)
- Polynomial Regression (degree 2)
- Multi-variable Linear Regression
- Random Forest Regressor (numerical + categorical)
- ANN — MLPRegressor (2 hidden layers: 64 + 32 units)

**Classification:**
- Random Forest Classifier with full feature set

**Clustering:**
- K-Means with PCA dimensionality reduction (2D visualisation)
- Hierarchical Agglomerative Clustering with dendrogram

---

## 💡 Key Findings

1. **Linear models outperform complex models** when features are strongly correlated — multi-variable linear regression (R²=0.959) beat both Random Forest (0.933) and ANN (0.946)
2. **Satisfaction Score** is the most predictive single feature for Monthly Spend
3. **Categorical variables matter** — adding Gender, Region, and Payment Method improved Random Forest performance significantly
4. **Subscription Length and Support Tickets** are important secondary predictors — longer subscriptions signal loyalty; more tickets may indicate high engagement
5. **K-Means k=3** produced the most interpretable customer segments for targeted marketing strategy

---

## 🛠️ Tech Stack

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **ML** — Scikit-learn (LinearRegression, PolynomialFeatures, RandomForestRegressor, RandomForestClassifier, MLPRegressor, KMeans)
- **Dimensionality Reduction** — PCA
- **Clustering** — KMeans, SciPy Hierarchical (dendrogram)
- **Preprocessing** — StandardScaler, OneHotEncoder
- **Evaluation** — R², MSE, Accuracy, F1, AUC-ROC, Confusion Matrix

---

## 📁 Repository Structure

```
├── Component_one.ipynb      # Full implementation notebook
├── README.md                # Project documentation
└── data/
    └── README.md            # Dataset download instructions
```

---

## 📥 Dataset

This project uses the **Streaming Service Customer Dataset** from Kaggle.

🔗 [Download from Kaggle](https://www.kaggle.com/datasets/akashanandt/streaming-service-data)

After downloading, place the CSV as:
```
data/
└── streaming_service_data.csv
```

---

## 👤 Author

**Muhammad Salahuddin**  
MSc Artificial Intelligence & Data Science — University of Hull  
[GitHub](https://github.com/msnoorani) | [LinkedIn](https://linkedin.com/in/msnoorani)
