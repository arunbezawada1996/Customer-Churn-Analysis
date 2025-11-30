# Customer Churn Analysis --- End-to-End ETL, Analytics & Machine Learning Project

## Overview

This project delivers a complete **Customer Churn Analytics Solution**
including: - A full **ETL pipeline** in SQL Server - A cleaned,
production-ready **data warehouse** - Power BI dashboard for **churn
insights & customer profiling** - A **Random Forest Machine Learning
Model** for predicting future churners - A reusable workflow for
continuous churn monitoring and marketing targeting

## Project Goals

### 1. Analyze customer data across key dimensions:

-   Demographic
-   Geographic
-   Account & Payment Info
-   Services

### 2. Profile churned customers & identify causes

### 3. Predict future churners using machine learning

## ETL Pipeline

ETL is executed using SQL Server Management Studio (SSMS) or SSIS.

### SQL Views

``` sql
CREATE VIEW vw_ChurnData AS
SELECT * FROM prod_Churn WHERE Customer_Status IN ('Churned', 'Stayed');
```

``` sql
CREATE VIEW vw_JoinData AS
SELECT * FROM prod_Churn WHERE Customer_Status = 'Joined';
```

## Machine Learning --- Random Forest Model

Uses Python, Jupyter Notebook, scikit-learn.

### Sample Code

``` python
rf_model = RandomForestClassifier(n_estimators=100, random_state=42)
rf_model.fit(X_train, y_train)
```

## Prediction Output

Predicted churners are exported as CSV for business action.
