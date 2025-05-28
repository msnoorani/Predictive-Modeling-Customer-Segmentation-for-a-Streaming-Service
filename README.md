# Predictive-Modeling-Customer-Segmentation-for-a-Streaming-Service
This project presents a comprehensive analysis of customer data from a streaming service, focusing on predictive modeling and unsupervised customer segmentation to optimize business decisions. Using both regression and classification models, we predict monthly customer spending and churn behavior. 
# Objectives:
1. Predictive Modeling

Forecast monthly spend using regression models: single-variable, multi-variable, polynomial, Random Forest, and Artificial Neural Networks (ANN).

Identify the best predictors among numerical and categorical features.

Predict customer churn using a Random Forest classifier.

2. Customer Segmentation

Apply K-Means and Hierarchical Clustering to identify customer groups.

Validate clusters using PCA visualization and dendrograms.

# Key Results:
Best Regression Model: Multi-variable Linear Regression (R² = 0.959), outperforming Random Forest and ANN due to strong linear feature relationships.

Best Churn Classifier: Random Forest Classifier (Precision, Recall, F1 = 1.0). However, results may reflect overfitting or data leakage.

Segmentation: Three customer clusters were identified using both K-Means and Hierarchical Clustering. Clusters show distinguishable behavioral patterns useful for marketing strategy.

# Tools & Techniques:
Data Processing: Pandas, NumPy, Scikit-learn

Modeling: Linear Regression, Polynomial Regression, Random Forest, MLPRegressor (ANN)

Classification: Random Forest

Clustering: K-Means, Hierarchical Clustering

Evaluation: R² score, Precision, Recall, F1-score, PCA for dimensionality reduction

Visualization: Matplotlib, Seaborn

# Recommendations:
Use multi-variable linear models for spend forecasting due to interpretability and performance.

Validate the churn classification model further to avoid relying on potentially overfit results.

Leverage clustering insights to design customer-specific promotions and retention strategies.
