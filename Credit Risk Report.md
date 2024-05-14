# Credit Risk Classification Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
    The purpose of this analysis is to use a Logistic Regression Model to train and evaluate
    loan risk in order to identify the creditworhtiness of borrowers.
    
* Explain what financial information the data was on, and what you needed to predict.
    The dataset is from historical lending activity from a peer-to-peer lending services company
    being used to predict loan that may or may not go into default.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    The dataset includes 77,536 records with information such as: borrower's income, debt to income ratio, the number of accounts held by the borrower, the number of derogatory marks on the borrowers accounts, the total debt and the loan status. These were used as the X variable.
    The number of records considered to be in "healthy status" was 75,037 and the remaining 2500 were considered "high-risk". These values were used as the y variable.

* Describe the stages of the machine learning process you went through as part of this analysis.
    The data was split into a training set and a test set using sklearn.model_selection and then fit into a Logistic Regression Model using sklearn.linear_model and predictions were made using lr_model.predict. A confusion matrix was generated and finally, the classifacation report was printed supporteing the accuracy of the model.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
    In addition to the aforementioned methods used in the process sklearn.metrics were used to create a confusion matrix and classification report to identify the reliability of the results.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Linear Regression Model:
    * The confusion matrix scores:
        - (TN) 18679 for '0' (Healthy Loan) predicted correctly
        - (FP) 80 for '0' (Healthy Loan) pedicted healthy incorrectly
        - (FN) 67 for '1' (At risk Loan) predicted at risk incorrectly
        - (TP 558) for '1' ( At risk Loan) predicted at risk correctly
        
    * The accuracy score was 0.99 predicted correctly overall
    * The precision of the (Healthy Loans) was 1.0, correctly predicted 100%
    * The recall score of the (Health Loans) was 1.0, correctly predicted 100%
    * The precision of the (At-risk Loans) was 0.87, correctly predicted 87%
    * The recall score of the (At-risk Loans) was 0.89, correctly predicted 89%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
    The Linear Regression Model is the best model to use in predicting the credibility of loans. With the accuracy rate of .99 along with high precision, recall and f1-score this confirms the successful performance of this model.
    
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    The problem is whether to assess the risk as well as the health for possible future transactions so predicting both zeros and ones is important for substantiating the viablility of loans.

 
