# Customer Churn Prediction System

## 📌 Project Overview

The **Customer Churn Prediction System** is a machine learning project designed to identify customers who are likely to leave a service.

The project analyzes customer demographics, usage behavior, support interactions, payment delays, subscription details, spending patterns, and other customer-related factors to predict churn.

The system also provides customer risk analysis and retention recommendations to help businesses take proactive actions toward customer retention.

---

## 🎯 Objectives

- Analyze customer behavior and churn patterns.
- Perform Exploratory Data Analysis (EDA).
- Identify important factors associated with customer churn.
- Preprocess numerical and categorical customer data.
- Train and compare multiple machine learning models.
- Improve the selected model through hyperparameter tuning.
- Predict whether a customer is likely to churn.
- Identify customers at different levels of churn risk.
- Generate retention recommendations for high-risk customers.

---

## 📊 Dataset

The dataset contains:

- **64,374 customer records**
- **12 columns**

### Features

| Feature | Description |
|---|---|
| CustomerID | Unique customer identifier |
| Age | Customer age |
| Gender | Customer gender |
| Tenure | Duration of customer relationship |
| Usage Frequency | Frequency of service usage |
| Support Calls | Number of customer support calls |
| Payment Delay | Payment delay information |
| Subscription Type | Customer subscription category |
| Contract Length | Length of customer contract |
| Total Spend | Total customer spending |
| Last Interaction | Number of days since last interaction |
| Churn | Target variable |

`CustomerID` was excluded from model training because it is an identifier rather than a meaningful predictive feature.

---

## 🔍 Exploratory Data Analysis

The project includes:

- Churn distribution analysis
- Numerical feature distributions
- Categorical feature analysis
- Churn rate by customer categories
- Correlation analysis
- Customer behavior analysis
- Feature importance analysis

---

## ⚙️ Data Preprocessing

The following preprocessing techniques were used:

- Removal of `CustomerID`
- Separation of features and target
- Numerical feature preprocessing
- Categorical feature preprocessing
- Missing-value handling
- Standardization of numerical features
- One-Hot Encoding of categorical features
- Train-test split with stratification

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

---

## 🤖 Machine Learning Models

Four machine learning algorithms were evaluated:

1. Logistic Regression
2. Random Forest Classifier
3. Decision Tree Classifier
4. K-Nearest Neighbors (KNN)

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score

---

## 📈 Model Performance

The initial model comparison produced the following results:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 82.70% | 81.37% | 82.34% | 81.85% |
| Random Forest | 99.85% | 99.95% | 99.74% | 99.84% |
| Decision Tree | 99.84% | 99.71% | 99.95% | 99.83% |
| KNN | 91.11% | 88.05% | 93.98% | 90.92% |

The Random Forest model was subsequently selected for further analysis and hyperparameter tuning.

---

## 🛠️ Hyperparameter Tuning

Randomized hyperparameter search with 3-fold cross-validation was used to tune the Random Forest model.

The tuned model achieved:

| Metric | Score |
|---|---:|
| Accuracy | **99.83%** |
| Precision | **99.93%** |
| Recall | **99.70%** |
| F1 Score | **99.82%** |

The tuning process was performed to evaluate whether model performance could be improved. In this experiment, the tuned model's accuracy was slightly lower than the original Random Forest result.

---

## 📊 Customer Risk Analysis

The system calculates the predicted probability of churn and assigns customers to risk categories:

- **Low Risk:** 0–30% churn probability
- **Medium Risk:** 30–60% churn probability
- **High Risk:** 60–100% churn probability

High-risk customers can be prioritized for proactive retention strategies.

---

## 💡 Retention Recommendations

Based on the predicted churn risk, the system provides recommendations such as:

- Proactively contact high-risk customers.
- Provide personalized offers or loyalty benefits.
- Maintain regular customer engagement.
- Monitor customer behavior for early signs of churn.
- Improve support and issue resolution.
- Use churn predictions to prioritize retention efforts.

---

## 🧪 Prediction System

The project includes a prediction function that accepts customer information and predicts whether the customer is likely to:

- **Stay**
- **Churn**

The system also provides prediction probabilities.

Example:

```text
Prediction: CUSTOMER LIKELY TO STAY
Prediction Probabilities: [1. 0.]
