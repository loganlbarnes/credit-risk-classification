# credit-risk-classification
UCI Data Analytics Module 20 Challenge

# Module 20 Report

## Overview of the Analysis

* # Explain the purpose of the analysis.
  * The analysis aims to use machine learning to predict loan risk based on various financial metrics. This helps financial institutions understand the potential risk of loan applications.


* # Explain what financial information the data was on, and what you needed to predict.
  * The dataset contains financial metrics such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable is loan_status, where 1 indicates a high-risk loan and 0 indicates a low-risk loan.

* # Provide basic information about the variables you were trying to predict (e.g., `value_counts`). 
  * The dataset has a class imbalance, with 75,036 low-risk loans and 2,500 high-risk loans.

* # Describe the stages of the machine learning process you went through as part of this analysis.
* # Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  * The analysis involves preparing the data, splitting it into training and testing sets, training logistic regression models on original and resampled data, and evaluating the model's performance using accuracy, precision, recall, and F1-score.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression Model with Original Data
  * Balanced Accuracy: Approximately 95.2%.
  * Confusion Matrix: True Negatives: 18,663, False Positives: 102, False Negatives: 56, True Positives: 563.
  * Classification Report: For healthy loans, the precision, recall, and F1-score are all approximately 100%. For high-risk loans, precision is 85%, recall is 91%, and F1-score is 88%.


* Machine Learning Model 2: Logistic Regression Model with Resampled Data
  * Balanced Accuracy: Approximately 99.45%.
  * Confusion Matrix: True Negatives: 74,614, False Positives: 422, False Negatives: 403, True Positives: 74,633.
  * Classification Report: The logistic regression model trained with oversampled data (where the number of high-risk and low-risk loans in the training set is equalized) is said to predict with near-perfect accuracy (99%).

## Summary

Both logistic regression models demonstrate high accuracy in predicting loan risks.

Model with Original Data: This model offers very high precision, recall, and F1-scores for healthy loans and also performs commendably in predicting high-risk loans.

Model with Resampled Data: Based on the provided information, the model trained with resampled data has near-perfect accuracy. Oversampling typically improves recall for the minority class by providing the model with more examples of that class.

Recommendation: Given the implications of not identifying high-risk loans, a model with a high recall for the high-risk category might be preferable.