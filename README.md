# Customer Churn Data Preparation & EDA

This repository contains the complete workflow for **Task 3: Customer Churn Data Preparation & EDA**. The project focuses on transforming the raw [Telecom Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) into a clean, feature-rich format suitable for machine learning models.

## 🎯 Project Objective
The goal is to perform end-to-end data preparation, including cleaning inconsistent types, engineering new features to capture customer behavior, and conducting exploratory data analysis (EDA) to identify drivers of attrition.

## 🧠 Key Learning Outcomes
* **Data Sanitization:** Identifying and fixing "strange" values (e.g., blank spaces in numeric columns) and inconsistent data types.
* **Advanced Feature Engineering:** Creating tenure buckets, spending groups, and transforming categorical data for modeling.
* **Statistical Visualization:** Using Seaborn and Matplotlib to create heatmaps, countplots, and boxplots to uncover churn patterns.

## 📋 Project Workflow

### 1. Data Understanding
* Load the dataset and perform initial inspections using `.info()` and `.describe()`.
* Identify hidden missing values, such as blank spaces (`" "`) in the `TotalCharges` column.

### 2. Data Cleaning
* **Type Conversion:** Fix data types by converting `TotalCharges` from object to float.
* **Missing Value Management:** Handle identified null values through dropping or imputation to ensure a complete dataset.

### 3. Feature Engineering
* **TenureGroup:** Categorize customers into buckets (e.g., 0–12 months, 13–24 months, etc.) to analyze loyalty trends.
* **AvgMonthlySpend:** Calculate a new metric: `TotalCharges / Tenure`.
* **Encoding:** * Convert binary "Yes/No" fields into `1/0`.
    * Apply one-hot encoding to multi-category columns like `Contract` and `InternetService`.

### 4. EDA & Visualization
* **Churn Distribution:** Countplot to visualize the balance of the target variable.
* **Contract Analysis:** Barplot comparing `Contract` types against `Churn` rates.
* **Correlation Heatmap:** Identify relationships between numeric features and customer attrition.
* **Spending Insights:** Boxplot showing `MonthlyCharges` distribution for churned vs. retained customers.

## 📂 Deliverables
* **Python Notebook:** `TASK_3.ipynb` containing the full documented code.
* **Cleaned Dataset:** `Cleaned_Churn_Data.csv` ready for predictive modeling.
* **Summary of Insights:** A breakdown of the top 5 findings from the EDA.

## 🛠️ Requirements
* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn

---
*This project was completed as part of a structured data science task flow focused on robust data preparation.*
