# Module 12 Report Template

## Overview of the Analysis

The analysis aims to assess the model's ability to distinguish between healthy and high-risk loans, considering the inherent imbalance in credit risk classification. The labeled dataset includes crucial variables like loan size, interest rate, borrower's income, debt-to-income ratio, account count, derogatory marks, and total debt, contributing to the prediction of loan status.

## Data 

* The dataset includes crucial variables such as loan size, interest rate, borrower's income, debt-to-income ratio, account count, derogatory marks, and total debt. These variables collectively play a role in predicting the loan status, classifying it as either a secure loan (value = 0) or a high-risk loan (value = 1).

* To create the Machine Learning model, the following steps were taken:

  - Data Separation:

   1. X: This variable includes all the "features" from the dataset that will be used to evaluate and predict the target variable, y.
   2. y: The "target" variable contains all the values from the loan_status column, representing the outcome the model aims to predict.

  - Dataset Splitting:

  - The dataset is divided into two distinct groups:

   1. Train: This subset constitutes the data used to train the machine learning model, typically comprising 75% of the dataset.
   2. Test: This subset is employed to assess the model's predictive capabilities based on its prior learning, typically constituting the remaining 25% of the dataset.

- These steps lay the foundation for training and evaluating the Machine Learning model on distinct sets of data to gauge its performance.


## Results

Two logistic regression models were implemented. The first utilized the original dataset, while the second employed a random oversampling technique to address the imbalance. The results and recommendations are outlined below:

Model 1 - Logistic Regression:

Balanced Accuracy: 95%
Precision (High-Risk): 85%
Recall (High-Risk): 91%

Model 2 - Logistic Regression with Random Oversampler:

Balanced Accuracy: 99%
Precision (High-Risk): 84%
Recall (High-Risk): 99%



## Summary

Model 2 outperforms Model 1 in balanced accuracy (99% vs. 95%) and recall for high-risk loans (99% vs. 91%). The oversampling technique enhances the model's ability to identify high-risk loans, though precision slightly decreases from 85% to 84%. Consideration of business priorities, resource constraints, and project goals is recommended before finalizing the model choice.

# Conditions/Caveats for Recommendation:

Business Context: Assess the relative importance of precision and recall based on the business context.

Resource and Computational Costs: Oversampling can be computationally expensive; evaluate the feasibility of implementation in a production environment.

In conclusion, Model 2 offers improved performance, with careful consideration of trade-offs and business priorities necessary for the final decision.