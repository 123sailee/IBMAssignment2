# Enterprise Data Preparation for Employee Attrition

## 1. Project Overview

This project focuses on preparing employee HR data for machine learning applications using the IBM HR Analytics Employee Attrition dataset.

The objective is to clean, transform, and organize raw employee data by handling missing values, duplicates, detecting outliers, encoding categorical variables, scaling numerical features, and creating derived HR features.

A reusable preprocessing pipeline is developed using Scikit-learn to automate the data preparation process.

## 2. Project Objectives

- Import and understand the HR employee dataset.
- Identify and handle missing values.
- Detect and handle duplicate records.
- Detect potential outliers using the IQR method.
- Encode categorical variables using One-Hot Encoding.
- Scale numerical features using StandardScaler.
- Create meaningful derived HR features.
- Build a reusable preprocessing pipeline.
- Export clean and processed datasets.

## 3. Dataset Description

**Dataset:** IBM HR Analytics Employee Attrition & Performance

**Source:** [Kaggle – IBM HR Analytics Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

| Description | Value |
|---|---:|
| Total Employee Records | 1,470 |
| Original Features | 35 |
| Target Variable | Attrition |
| Missing Values | 0 |
| Duplicate Records | 0 |

## 4. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- GitHub

## 5. Data Preparation Workflow

1. Dataset Import
2. Dataset Inspection
3. Missing Value Analysis and Handling
4. Duplicate Record Removal
5. Outlier Detection using IQR
6. Feature Engineering
7. Categorical Variable Encoding
8. Numerical Feature Scaling
9. Preprocessing Pipeline Creation
10. Processed Dataset Export

## 6. Data Cleaning

The following operations were performed:

- Checked missing values across all columns.
- Handled missing numerical values using median imputation.
- Handled missing categorical values using mode imputation.
- Identified and removed duplicate records.
- Detected potential outliers using the Interquartile Range (IQR) method.

Potential outliers were identified and reported rather than automatically removed, preserving valid employee records.

## 7. Feature Engineering

Three new HR features were created.

### A. Total Satisfaction

Calculated using:
- Environment Satisfaction
- Job Satisfaction
- Relationship Satisfaction
- Work-Life Balance

### B. Tenure Ratio

Measures the proportion of an employee's total working experience spent at the current company.

Formula:

Tenure Ratio = Years at Company / Total Working Years

A value of zero is assigned when total working years is zero.

### C. Career Start Age

Calculated as:

Career Start Age = Age - Total Working Years

## 8. Data Transformation

### Categorical Encoding

One-Hot Encoding was used to convert categorical variables into numerical representations.

### Numerical Scaling

StandardScaler was applied to standardize numerical features.

### Target Variable Encoding

- Yes = 1
- No = 0

## 9. Preprocessing Pipeline

A reusable preprocessing pipeline was developed using Scikit-learn.

**Numerical Pipeline:**
- SimpleImputer (Median)
- StandardScaler

**Categorical Pipeline:**
- SimpleImputer (Most Frequent)
- OneHotEncoder

**Pipeline Components:**
- ColumnTransformer
- Pipeline

The fitted preprocessing pipeline was saved as a `.pkl` file for reuse.

## 10. Generated Deliverables

| File | Description |
|---|---|
| Clean_Dataset.csv | Cleaned dataset with engineered features |
| Processed_Dataset.csv | Encoded and scaled dataset |
| Data_Cleaning_Report.txt | Data cleaning summary |
| Feature_Engineering_Report.txt | Feature creation and transformation details |
| Pipeline_Documentation.txt | Preprocessing pipeline documentation |
| Employee_Attrition_Preprocessing_Pipeline.pkl | Saved preprocessing pipeline |
| Enterprise_Data_Preparation.ipynb | Complete Python notebook |

## 11. Results

**Clean Dataset:**
- 1,470 employee records
- 38 columns, including three engineered features
- Zero missing values
- Zero duplicate records

**Processed Dataset:**
- 1,470 employee records
- 54 transformed input features
- 1 target variable
- 55 columns in total

## 12. Conclusion

This project demonstrates a structured approach to enterprise HR data preparation. Data cleaning, outlier detection, feature engineering, categorical encoding, numerical scaling, and pipeline development were performed to prepare the employee attrition dataset for future machine learning applications.

## 13. Author

**Sailee Abhale**

B.Tech – Artificial Intelligence and Data Science

**Project:** IBM Data Science Advanced Programming – Assignment 2
