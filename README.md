# credit-risk-classification
Module 20 Challenge: Supervised Learning

## Overview

The goal of this challenge is to use a Machine Learning technique to predict whether a loan would be healthy or high-risk. The lending dataset used to build a model that can identify/predict creditworthiness  includes information such as interest rate, borrower income, debt-to-income ratio, number of account etc. A preview of the dataset used is shown below.

![Lending data preview](<Screenshot 2024-07-22 013912.png>)

 A logistic regression model using the original data was used to split, train, and test sets, and the accuracy of its prediction determined by generating a confusion matrix and classification report.

 ## Results

 * Summary of classfication matrix

 The confusion matrix tells us about the perfomance of a classification model. The matrix below shows us that:
  - 18663 loans were actually healthy(class 0). Thus True Positives.
  - 563 loans were actually high-risk (class 1). Thus True Negatives.
  - 102 loans were actually healthy (class 0) but the model predicted them as high-risk (class 1). Thus False Negative.
  - 56 loans were actually high-risk(class 1) but the model redicted them as healthy. Thus False Positives.
 
 ![Classification Matrix](<Screenshot 2024-07-22 020315.png>)


* Summary of Classification Report

The metrics below are used to evealuate how good the model is at identifying differrent classes.

    * Accuracy:

    The accuracy of 0.99 means 99% of the predictions were correct.

    * Precision:

    The prediction of 1.00 for Class 0(healthy) means that all predictioed instances as class 0 were actually class 0. The precision for class 1 (high-risk) indicates that out of the loans the model predicted as high-risk, 85% were truly high-risk. 

    * Recall Score: 

    The recall values for a class tells us the proportion of actual positives that were identified by the model. The recall of 0.99 for class 0(healthy) means the model captured 99% of the actual healthy loans, while the 0.91 for class i(high-risk) identified 91% of the actual high-risk loans.


![Classification Report](<Screenshot 2024-07-22 020339.png>)


## Summary

Overall, based on the above metrics, the logistic regression model does  a good job at  predicting healthy versus high-risk loans. However, the high accuracy weighted heavily by class 0(healthy) might be misleading. This could lead to providing loans to people who are actually high risk but were misrepresented as healthy. I propose to resample the data again and perform the logisctic regression, or use a different model. 

