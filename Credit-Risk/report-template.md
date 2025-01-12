# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose was to train a machinge learning model to classify good or hirh-risk credit loans.

* Explain what financial information the data was on, and what you needed to predict.

These were all of the columns in the csv dataset. 

-loan_size,
-interest_rate,
-borrower_income,
-debt_to_income,
-num_of_accounts,
-derogatory_marks,
-total_debt,
-loan_status

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The target variable, loan_status, had the following distribution:

Healthy Loans (0): 75,036 instances
High-Risk Loans (1): 2500 instances

* Describe the stages of the machine learning process you went through as part of this analysis.

Data Preprocessing:

Created labels (y) from the loan_status column.
Created features (X) by dropping the loan_status column.
Split the data into training and testing sets using train_test_split.
Scaled the features using StandardScaler to normalize the data.

Model Selection and Training:

Chose Logistic Regression with a random state of 1
Fit the model using the training data
Tested 19384 instances


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
    * Logistic Regression Model:
    * Accuracy: 99%
    * Precision for Healthy Loans (0): 1.00
    * Recall for Healthy Loans (0): 0.99
    * Precision for High-Risk Loans (1): 0.84
    * Recall for High-Risk Loans (1): 0.94

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
The model predicted the healthy loans with a 99% accuracy. Looking at the classification report shows this information and tells you that the model is very accurate when predicting healthy loans. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

With this model, it does solve the probelm we are trying to solve. 
We can know that if the model predicts a healthy loan, that it is 99% accurate and therefore we can give out that loan to the borrower. But predicting high-risk loans (1's) is crucial for minimizing financial losses, so enhancing the model's ability to accurately predict this class may be necessary.

If you do not recommend any of the models, please justify your reasoning.
