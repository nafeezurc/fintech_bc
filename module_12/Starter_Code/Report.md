# Module 12 Report

## Overview of the Analysis

The purpose of this analysis is to classify loan data as a healthy or unhealthy loan. 

The data included the size of the loan, the interset rates, borrower income, borrow debt, the debt to income ratio, the number of accounts the borrow has, and the number of derogatory marks.

The goal was to predict the loan status, that is, whether a loan was healthy or unhealthy. A 0 indicates a healthy loan, whereas a 1 indicates an unhealthy loan.

The stages of the machine learning process included Model-Fit-Predict-Evaluate. The logistic regression model was chosen for the classifier, and the data was split into train and test catagories.
The model was then fit on the training data, and then predicted based on the test data. The model results were then evaluated through its accuracy score, confusion matrix, and classification report.
The data was also fitted through a Random Oversampler to make the data more balanced, and the same process was repeated over the oversampled dataset.

The main methods to note are LogisticRegression(), which is the model that was used for classification, and RandomOverSampler(), which oversampled the training data to make the data more balanced between
1's and 0's.

## Results

* Machine Learning Model 1: Logistic Regression (Original Data)
  * Accuracy: 0.952
  * Precision: 0.99 (0: 1.00; 1: 0.85)
  * Recall: 0.99 (0: 0.99; 1: 0.91)
 
* Machine Learning Model 2: Logistic Regression (Oversampled Data)
  * Accuracy: 0.994
  * Precision: 0.99 (0: 1.00; 1: 0.84)
  * Recall: 0.99 (0: 0.99; 1: 0.99)

## Summary

Model 2, the one with the oversampled data, seemed to perform the best. Having a higher accuracy, a higher recall, and as a result a higher f1 score, Model 2 outperforms Model 1 for this dataset. 
The performance does depend on the problem we are trying to solve as detecting an actual bad loan is more difficult due to the imbalance of data. By balancing the data through oversampling, the model is able to predict
more bad loans among the bad loan subdata. Therefore, I recommend using Model 2 for this problem.
