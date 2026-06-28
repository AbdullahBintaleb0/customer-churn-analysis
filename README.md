# Customer Churn Prediction

> A comparative study of 10 machine learning classification models for customer churn prediction using data mining techniques.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Enabled-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## Overview

Customer churn is one of the most critical business challenges because losing customers directly impacts revenue and growth. This project develops a complete data mining pipeline to predict customer churn using machine learning.

The project follows the Knowledge Discovery in Databases (KDD) methodology, including:

* Data exploration
* Data preprocessing
* Feature engineering
* Feature selection
* Model training
* Model evaluation
* Business interpretation

---

## Authors

* Mohammed Adimi (4410638)
* Abdullah Bintalib (4410891)
* Ziyad Chihani (4312645)

**Course:** AI 306 – Data Mining
**Academic Year:** 2025–2026

---

## Problem Statement

Acquiring new customers can cost 5–7 times more than retaining existing customers. Therefore, predicting customers who are likely to leave allows businesses to take proactive actions to improve customer retention.

The goal of this project is to identify at-risk customers before churn occurs.

---

## Dataset

* **Source:** Kaggle Customer Churn Business Dataset
* **Records:** 10,000
* **Original Features:** 32
* **Missing Values:** 2,045
* **Target Variable:** Churn (Yes / No)

---

## Key Features

* tenure_months
* csat_score
* monthly_logins
* payment_failures
* last_login_days_ago
* avg_session_time
* email_open_rate
* avg_resolution_time

---

## Data Preprocessing Pipeline

### 1. Remove Irrelevant Features

* Removed IDs and low-importance features.

### 2. Handle Missing Values

* Imputed missing values in complaint_type.

### 3. Encode Categorical Variables

* Applied label encoding and one-hot encoding.

### 4. Feature Scaling

* Used StandardScaler.
* Scaling was applied only on training data to prevent data leakage.

### 5. Feature Selection

* Selected the top 8 features using XGBoost feature importance.

---

## Machine Learning Models

The following models were trained and evaluated:

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting
* AdaBoost
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)
* Naive Bayes
* Multi-Layer Perceptron (MLP)
* XGBoost

---

## Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* AUC-ROC

---

## Results

| Model               | Accuracy | F1-Score | AUC-ROC |
| ------------------- | -------- | -------- | ------- |
| XGBoost             | 0.76     | 0.38     | 0.81    |
| Gradient Boosting   | 0.75     | 0.38     | 0.81    |
| AdaBoost            | 0.74     | 0.38     | 0.80    |
| Random Forest       | 0.83     | 0.31     | 0.76    |
| SVM                 | 0.73     | 0.31     | 0.76    |
| Decision Tree       | 0.77     | 0.32     | 0.69    |
| Logistic Regression | 0.68     | 0.26     | 0.70    |
| Naive Bayes         | 0.89     | 0.11     | 0.75    |
| MLP                 | 0.89     | 0.10     | 0.69    |
| KNN                 | 0.90     | 0.01     | 0.59    |

---

# Best Model: XGBoost

* Accuracy: 76%
* Recall: 74%
* F1-Score: 0.38
* AUC-ROC: 0.81

XGBoost achieved the highest overall performance and demonstrated strong capability in identifying churned customers.

---

## Key Findings

* Data preprocessing significantly improved model performance.
* High accuracy does not always indicate a good model.
* Ensemble methods outperformed traditional classifiers.
* Recall is the most important metric in churn prediction.
* XGBoost provided the best balance between recall and overall performance.

---

## Business Recommendations

* Deploy monthly churn scoring using XGBoost.
* Target short-tenure customers with personalized offers.
* Reduce payment failures through reminders and easier payment options.
* Improve customer satisfaction and support quality.
* Focus retention campaigns on high-risk customers.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* Matplotlib
* Seaborn
* Imbalanced-Learn (SMOTE)

---

## Project Structure

```text
customer-churn-prediction/
│
├── data/
├── notebooks/
├── src/
├── images/
├── report/
├── presentation/
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Installation

```bash
git clone https://github.com/yourusername/customer-churn-prediction.git

cd customer-churn-prediction

pip install -r requirements.txt
```

---

## Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
imbalanced-learn
jupyter
```

---

## Future Improvements

* Hyperparameter optimization
* Real-time prediction pipelines
* Time-series customer behavior analysis
* Deep learning approaches
* Web deployment using Flask or Streamlit

---

## Conclusion

This project demonstrates the importance of data preprocessing and machine learning in customer churn prediction. Among ten classification algorithms, XGBoost achieved the best overall performance and provided actionable business insights for customer retention.

---

## References

* Chen, T., & Guestrin, C. XGBoost: A Scalable Tree Boosting System.
* Pedregosa et al. Scikit-Learn: Machine Learning in Python.
* Kaggle Customer Churn Business Dataset.
