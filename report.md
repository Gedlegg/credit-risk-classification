# Credit Risk Analysis

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

### Purpose of the Analysis

The purpose of this analysis was to build a machine learning model to predict the risk status of loans, specifically to classify loans as either "healthy" (0) or "high-risk" (1). This predictive capability can help financial institutions manage risk and make informed lending decisions.

### Financial Information in the Data

The data used in this analysis included the following financial information:

* **Loan Size** : The amount of money borrowed.
* **Interest Rate** : The interest rate applied to the loan.
* **Borrower Income** : The income of the borrower.
* **Debt-to-Income Ratio** : The ratio of the borrower's total debt to their total income.
* **Number of Accounts** : The number of credit accounts the borrower has.
* **Derogatory Marks** : Negative marks on the borrower's credit report.
* **Total Debt** : The total amount of debt the borrower has.
* **Loan Status** : The target variable indicating whether the loan is healthy (0) or high-risk (1).

### Variables to Predict

The target variable to predict is `loan_status`. Here's a breakdown of the value counts for this variable:

* `0` (Healthy Loan): 75,036 instances
* `1` (High-Risk Loan): 2,543 instances

### Stages of the Machine Learning Process

1. **Data Preparation** :

* Read the CSV file and review the data.
* Separate the data into features (`X`) and labels (`y`).

1. **Data Splitting** :

* Split the data into training and testing sets using `train_test_split`.

1. **Model Training** :

* Create and fit a logistic regression model using the training data.

1. **Model Prediction** :

* Use the fitted model to make predictions on the testing data.

1. **Model Evaluation** :

* Evaluate the model's performance using a confusion matrix and classification report.

### Methods Used

The primary method used in this analysis was `LogisticRegression` from the Scikit-Learn library. This algorithm was chosen for its simplicity and effectiveness in binary classification problems.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* **Logistic Regression Model** :
* **Accuracy** : 0.9922 (99.22%)
* **Precision and Recall Scores** :
  *  **Precision** :
  * Class 0 (Healthy Loan): 1.00
  * Class 1 (High-Risk Loan): 0.86
    *  **Recall** :
  * Class 0: 1.00
  * Class 1: 0.91
    *  **F1-Score** :
  * Class 0: 1.00
  * Class 1: 0.88

## Summary

### Model Performance

The logistic regression model performed exceptionally well, achieving an overall accuracy of 99.22%. The precision and recall scores for both classes were high, with particularly strong performance for the healthy loan class (Class 0):

* **Class 0 (Healthy Loan)** :
* **Precision** : 1.00, indicating no false positives.
* **Recall** : 1.00, indicating no false negatives.
* **F1-Score** : 1.00, indicating perfect precision and recall balance.
* **Class 1 (High-Risk Loan)** :
* **Precision** : 0.86, meaning 86% of the loans predicted as high-risk were actually high-risk.
* **Recall** : 0.91, meaning the model correctly identified 91% of the actual high-risk loans.
* **F1-Score** : 0.88, indicating a good balance between precision and recall.

### Confusion Matrix

The confusion matrix provided the following results:

* **True Negatives (TN)** : 14926
* **False Positives (FP)** : 75
* **False Negatives (FN)** : 46
* **True Positives (TP)** : 461

### Recommendation

The logistic regression model is recommended due to its high accuracy and excellent performance in predicting both healthy and high-risk loans. The model's precision and recall for high-risk loans are sufficient for practical applications, although there is room for improvement in reducing false positives and false negatives.

Given the results, the model's performance does not seem to heavily depend on the specific problem, as it performs well in predicting both healthy and high-risk loans. However, if the goal is to minimize the number of high-risk loans that are not identified (false negatives), further model tuning or using more complex models could be considered.
