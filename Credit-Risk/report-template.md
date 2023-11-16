# Module 12 Report Template

## Overview of the Analysis

 The purpose of this analysis is to determine whether a borrower is creditworthy, as well as, determine if the algorithm used does good job of predicting creditworthiness. Data used came from a peer to peer lending organization and included, loan amounts, interest rate,  borrower income, number of accounts and derogatory history. The purpose was to be able to predict whether the borrower would repay the loan.  

Value counts function was used to determine the number of loans in each category. 

With just over 75,000 loans the data was split into training and testing sets. A training set was used to build an initial logistic regression model using the LogisticRegression module. Logistic Regression Model 1 was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.

This intial model was drawing from a dataset that had  approximately 75,000 low-risk loans and 2,500 high-risk loans. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module. 

The resampled data was used to build a new logistic regression model. Logistic Regression Model 2 was used to determine whether a loan in the testing set would be a low risk or high risk loan. 

## Results

Logistic Regression Model 1:

Precision: At 93% on average in predicting.  
100% precise on healthy loans, the only 87% accurate in predicting high-risk loans. 
Overall Accuracy: 94%
Recall: 95% on average this model had 100% recall in predicting low-risk loans, but only 89% in predicting higher-risk loans.


Logistic Regression Model 2:

Precision: Also 93% on average.  Also 100% precise in predicting healthy loans, and similarly 87% accurate on higher hisk loans. 
Accuracy: 100%
Recall: 100%

Summary
Logistic Regression Model 2 is less likely to predict false negative results. 

Neither model scores well in predicting unhealthy loans, as one bad loan can negate the profit upside of many, many healthy loans.  

I do not recommend either model, and while I do not know this industry well, I would think the expectation would be to predict which loans a re likely to go unpaid at the 99% or better level. 
