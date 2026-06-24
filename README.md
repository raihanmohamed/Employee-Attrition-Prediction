Employee Attrition Prediction

A machine learning project that analyzes HR data to understand and predict employee attrition (turnover), and translates the findings into actionable HR recommendations.

Overview

This project explores why employees leave a company, builds and compares classification models to predict attrition, and identifies the key factors driving it. The final goal is not just a working model, but business insights that an HR team can actually act on.

Dataset


Source: IBM HR Analytics Employee Attrition dataset (CSV)
Target column: Attrition (Yes/No), converted to 1/0
Mix of numeric (e.g. Monthly Income, Age, Years at Company) and categorical (e.g. Department, Job Role, Marital Status) features


Project Workflow

1. Data Loading & Exploration


Loaded and inspected the dataset (shape, columns, data types)
Calculated overall attrition rate and checked for class imbalance


2. Data Cleaning & Preprocessing


Handled missing values
Dropped non-predictive columns (EmployeeNumber, Over18, StandardHours)
Converted target column to binary (1/0)
One-Hot Encoded categorical features
Scaled numeric features with StandardScaler


3. Exploratory Data Analysis (EDA)


Attrition rate by Department and Job Role
Relationship between attrition and Monthly Income, Work-Life Balance, and Years at Company
Documented specific, data-backed business insights (not generic observations)


4. Model Building


Train/test split (80/20)
Handled class imbalance using class_weight='balanced'
Trained and compared three models:

Logistic Regression (baseline, most explainable)
Random Forest Classifier
Gradient Boosting Classifier





5. Model Evaluation


Compared models using Precision, Recall, F1-Score, and ROC-AUC
Selected the best-performing model and extracted feature importances
Ranked the top 10 features driving attrition


6. Visualization


Attrition rate by Department & Job Role (bar chart)
Monthly Income distribution: left vs. stayed (box plot)
Confusion matrix heatmap for the best model
Top 10 feature importances (horizontal bar chart)
ROC curve comparing all three models


7. HR Insights & Recommendations


Identified the strongest predictors of attrition
Flagged the department/role HR should prioritize for retention
Assessed whether salary alone explains attrition
Provided concrete, actionable HR recommendations
Noted model limitations for responsible use by non-technical stakeholders


Key Findings


Sales and HR have higher attrition than other departments; Research & Development retains employees best.
Sales Representatives have the highest turnover of any role.
Lower-paid employees are more likely to leave, but pay alone doesn't explain attrition.
Frequent overtime is strongly linked to higher attrition.
Most departures happen within the first 1–2 years, pointing to an early-career retention gap.


Recommendations


Build targeted retention programs for Sales roles and early-career (0–2 year) employees.
Address excessive overtime through workload redistribution or improved compensation/work-life balance options.


Tech Stack


Python
Pandas, NumPy — data handling
Scikit-learn — preprocessing, modeling, evaluation
Matplotlib / Seaborn — visualization
Jupyter Notebook
