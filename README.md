# Credit Risk and Fraud Detection Analysis

## Objective

The main goal of this analysis is to detect irregular activity and potential fraud in a dataset containing credit history information from Banco Uno clients. The dataset consists of 2,395 records and 25 columns, including demographic data, payment history, billing amounts, payment amounts, and a target variable indicating default status.

## Data Preparation

- **Data Cleaning:**  
  - Removed unnecessary columns (e.g., row index).
  - Standardized column names to uppercase for consistency.
  - Checked for missing values and duplicates.
  - Ensured correct data types for each variable.

- **Exploratory Analysis:**  
  - Used `.info()` and `.describe()` to understand data structure and summary statistics.
  - Identified outliers using the Interquartile Range (IQR) method for all numeric columns.
  - Created a separate DataFrame (`df_outliers_all`) containing all records that are outliers in at least one numeric column.

## Machine Learning Model

- **Model Selection:**  
  - Used a Random Forest Classifier to predict the likelihood of default (fraud/suspicious activity).
  - Encoded categorical variables (`SEX`, `EDUCATION`, `MARRIAGE`) numerically.
  - Split the data into training and test sets (70%/30%).

- **Model Training and Prediction:**  
  - Trained the model on the training set.
  - Predicted the target variable for the entire dataset.
  - Created a DataFrame (`df_suspicious`) with records predicted as fraud or suspicious activity.

## Key Findings

- **Outlier Analysis:**  
  - Outliers were not removed, as they may represent potential fraud or irregular activity.
  - Outliers were analyzed for unusual combinations (e.g., very high credit limits for young clients, inconsistent payment patterns).

- **Fraud/Suspicious Detection:**  
  - The machine learning model identified a subset of clients with a high probability of default or suspicious behavior.
  - These records are available in the `df_suspicious` DataFrame for further investigation.

## Recommendations

- **Further Investigation:**  
  - Review the flagged records in detail, especially those with multiple outlier features or inconsistent demographic and financial data.
  - Consider combining model predictions with business rules or expert review for more robust fraud detection.

- **Model Improvement:**  
  - Experiment with other algorithms and feature engineering to improve prediction accuracy.
  - Regularly update the model with new data to adapt to evolving fraud patterns.

---

## Summary

This analysis provides a structured approach to identifying potential fraud and irregular activity in credit data using both statistical and machine learning techniques. The results can help financial institutions prioritize cases for further review and strengthen their risk management processes.
