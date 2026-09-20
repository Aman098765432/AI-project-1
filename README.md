# Telco Customer Churn Analysis

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

The exploratory analysis helps identify patterns between customer characte
