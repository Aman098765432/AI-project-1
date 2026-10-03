Week 1 # Telco Customer Churn Analysis

## 📌 Project Overview

This project focuses on analyzing customer churn using the **Telco Customer Churn dataset**. The main objective is to understand customer behavior, identify the factors that contribute to customer churn, and visualize important patterns in the dataset.    

The project uses **Python, Pandas, NumPy, Matplotlib, and Seaborn** for data analysis and visualization.

## 🎯 Objectives

* Understand the structure of the Telco Customer Churn dataset.
* Clean and preprocess the data.
* Explore customer demographics and service information.
* Analyze the relationship between different features and customer churn.
* Create meaningful data visualizations.
* Identify important factors associated with customer churn.
* Prepare the dataset for future machine-learning prediction.

## 📊 Dataset

The project uses the **Telco Customer Churn dataset**, which contains information about telecommunications customers.

Important features include:

* Customer demographics
* Gender
* Senior citizen status
* Partner and dependents
* Tenure
* Phone and internet services
* Online security and backup
* Device protection
* Technical support
* Contract type
* Payment method
* Monthly charges
* Total charges
* Churn status

The target variable is:

**Churn** – indicates whether a customer left the company.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / Kaggle Notebook

## 🔍 Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas and its basic structure is examined.

```python
import pandas as pd

df = pd.read_csv("WA_Fn-UseC_-Telco-Customer-Churn.csv")

print(df.shape)
df.head()
```

### 2. Data Exploration

The dataset is explored using:

* `head()`
* `shape`
* `info()`
* `describe()`
* Missing-value analysis
* Duplicate-value checking

This helps understand the quality and structure of the data.

### 3. Data Cleaning

The data is checked for missing and inconsistent values. Columns are converted into appropriate data types where necessary.

Special attention is given to the **TotalCharges** column because some values may be stored as strings or contain missing values.

### 4. Exploratory Data Analysis

Different customer characteristics are analyzed to understand their relationship with churn.

Examples include:

* Churn by gender
* Churn by senior citizen status
* Churn by contract type
* Churn by internet service
* Churn by tenure
* Churn by monthly charges
* Churn by payment method

### 5. Data Visualization

Multiple visualizations are created to make the analysis easier to understand.

The project includes charts such as:

* Bar charts
* Count plots
* Distribution plots
* Histograms
* Churn comparisons
* Feature-based visualizations

These visualizations help identify patterns and trends in customer behavior.

## 📈 Key Analysis

The analysis focuses on understanding why some customers are more likely to leave the company.

Factors examined include:

* **Contract type**
* **Customer tenure**
* **Monthly charges**
* **Internet service**
* **Payment method**
* **Technical support**
* **Online security**
* **Customer demographics**

The visual analysis provides insights into the characteristics of customers associated with higher churn.

## 💡 Insights

The exploratory analysis helps identify patterns between customer character

# Telco Customer Churn Prediction — Week 2

This project focuses on predicting customer churn using machine learning.

### Work Completed

* Data preprocessing and feature engineering
* Logistic Regression
* Decision Tree
* Random Forest
* Confusion Matrix and ROC-AUC analysis
* Threshold analysis
* Class imbalance handling
* Feature importance analysis

### Best Results

* Logistic Regression Accuracy: **80.7%**
* Random Forest Accuracy: **80.7%**
* Random Forest AUC: **0.8422**

### Tools

Python, Pandas, NumPy, Scikit-learn, Matplotlib, and Kaggle.
## Week 3: Model Optimization and Unsupervised Learning

In Week 3, I focused on improving model evaluation, hyperparameter tuning, customer segmentation, and dimensionality reduction for the Telco Customer Churn project.

- Split-to-split accuracy across 20 random seeds ranged from **0.780 to 0.828**, with a standard deviation of **0.0104**.
- 5-fold cross-validation results:
  - Logistic Regression: **0.8464 ± 0.0129 AUC**
  - Random Forest: **0.8464 ± 0.0114 AUC**
  - XGBoost: **0.8502 ± 0.0117 AUC**
- Logistic Regression validation curve selected **C = 10.0**.
- Random Forest Grid Search:
  - Best CV AUC: **0.8468**
  - Time: **79 seconds**
  - Best parameters: `max_depth=8`, `max_features='sqrt'`, `min_samples_leaf=20`
- Random Forest Random Search:
  - Best CV AUC: **0.8464**
  - Time: **83 seconds**
  - Best parameters: `max_depth=15`, `max_features≈0.213`, `min_samples_leaf=15`
- XGBoost early stopping selected **247 trees**.
- Tuned XGBoost achieved the highest CV AUC of **0.8502**.
- Final XGBoost test performance:
  - AUC: **0.8483**
  - Recall: **0.521**
  - Precision: **0.659**
- K-Means clustering selected **k = 4** customer segments:
  - High-charge, newer customers: **43% churn**
  - New, low-service customers: **32% churn**
  - Long-tenure, high-value customers: **14% churn**
  - Long-tenure, low-cost customers: **5% churn**
- PCA showed that **15 of 30 components** are required to explain at least 90% of the variance.
- The final model was saved as `churn_model.joblib` for deployment in Week 4.

### Biggest Lesson

A single train/test split can give a misleading estimate of model performance. Cross-validation gives a more reliable estimate by showing both the average performance and its variation.

Compared with Week 2, tuning produced only a small improvement in AUC, from approximately **0.842 to 0.8483**. This showed me that more complex tuning does not always result in a large performance improvement.

