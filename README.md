# credit-risk-classification
Module 20 for the U of M Data Analytics and Visualization Bootcamp

## Overview of the Analysis


The purpose of this analysis was to predict whether an individual would default on their bank loan. The data had features that included the following:


*loan_size: size of the loan as measured in United States Dollars
*interest_rate: Rate of interest at the time the loan was issued	
*borrower_income: The income of the loan holder	
*debt_to_income: The total amount of debt of the loan holder divided by the income of the loan holder	
*num_of_accounts: The number of accounts the loan holder has with the bank	
*derogatory_marks: Number of times that the loan holder has been delinquent in their payments	
*total_debt: Total amount of debt of the loan holder	
*loan_status: Binary response variable. A value of 0 in the loan_status column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.


We notice that there are imbalanced classes in this problem. Specifically, the 0's outnumber the 1's in the train and testing sets by about 30 to 1. Therefore, it is more important to classify the 1's correctly, and this will be the focus of our analysis.

## Results


* Machine Learning Model 1: Logistic Regression
    - Accuracy: 0.99, meaning there is a 1% chance of incorrectly classifying the target variable.
    - The precision of 1's is 0.85=563/(102+563), or there is a 15% chance of a false positive. 
    - The recall of 1's is (0.91 = 563/(56+563)) indicates that there is a 9% chance of a false negative.

* Machine Learning Model 2: knn
    - Accuracy: 0.99, meaning there is a 1% chance of incorrectly classifying the target variable.
    - The precision of 1's is 0.84=(574/(107+574)), or there is a 16% chance of a false positive. 
    - The recall of 1's is (0.93=574/(45+574)), or there is a 7% chance of a false negative.

* Machine Learning Model 3: Random Forest Classifier
    - Accuracy: 0.99, meaning there is a 1% chance of incorrectly classifying the target variable.
    - The precision of 1's is (0.85=557/(100+557)), or there is a 15% chance of a false positive.
    - The recall of 1's is (0.90=557/(62+557)), or there is a 10% chance of a false negative.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* All models have an accuracy of 0.99, but it's better to look at precision and recall for 1's since the classes are so unbalanced in favor of the 0's. A false positive in the context of our data means that the model predicts a 1 when the point is actually a 0. A false negative occurs when the model predicts a 0 when it is actually a 1. Since the 1's are so much rarer than the 0's, I think it is better to minimize the false negatives in this case. Of the 3 models, the knn model has the highest recall for the 1's, meaning that there is the lowest rate of a false negative. The models have similar performance otherwise. Therefore, the knn model is preferred. 
