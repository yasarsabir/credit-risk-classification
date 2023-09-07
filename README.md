# credit-risk-classification

## Overview 

In this task various techniques were used to train and evaluate data using a  Logistical Regression model to assess loan risk. This report explains which techniques and models I have used and the accuracy of each. 

Using a dataset (lending_data.csv) of historical lending activity from a peer-to-peer lending services company, a model was built to identify the creditworthiness of borrowers.

In this data set all loans were categorised as "loan_status" of 0 or 1, where a value of 0 meant a "healthy loan", and 1 meant a "high risk loan". 

There were 77,536 loans assessed, of which only 2500 were considered high risk, therefore the data was highly imbalanced towards healthy loans.

The model was asked to predict the loan_status (the target variable), ie the risk of a loan, based on the following given financial information: loan_size, interest_rate,	borrower_income,	debt_to_income,	number_of_accounts, derogatory_marks	and total_debt.

The data was split into Training and Testing Sets and then a logistical regression model was used to analyse the data, this is termed Model 1. 

The model, fit, predict process was used for each model. 

Given the imbalanced nature of the data a second model was used usign the RandomOverSampler to retrain the data set, in which case 56277 datapoints were asessed for each of the healthy and high risk loans. 

Each model was then compared.  

## Results

* Machine Learning Model 1:
  * Accuracy = 94.4%,
  * Precision - Healthy Loan = 1.00, High-Risk Loan = 0.87
  * Recall scores - Healthy Loan = 1.00, High-Risk Loan  = 0.89.


* Machine Learning Model 2: Oversampled Model.
  * Accuracy = 99.6%,
  * Precision - Healthy Loan = 1.00, High-Risk Loan = 0.87
  * Recall scores - Healthy Loan = 1.00, High-Risk Loan  = 1.00.
 
* 

## Summary

When using the oversampled model of the high risk loans, the overall accuracy improved from 94.4% to 99.6%, additionally in model 2, the recall for the high risk loans increased to 100% from 89% and the false negatives reduced from 67 to 2. Therefore model 2 preforms the best. 
Performance of the model is dependent on the real life scenario, here we need to be able to predict the high risk loans more accurately than healthy loans (ie the '1's').
If you do not recommend any of the models, please justify your reasoning.
