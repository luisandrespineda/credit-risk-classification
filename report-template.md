# Module 12 Report Template

## Overview of the Analysis

The purpose of the analysis was to build a model that could be used to predict whether a loan would be fully paid off or become deliquent.

The given data set provided 8 pieces of information for each individual loan. This included the amount of the loan, interest rate, income of the borrower, the number of accounts, derogatory marks, and the total debt of the borrower. The final column listed the health of the loan, "0" indicating a healthy loan while "1" indicated a loan at high risk of defaulting. The information collected is relevant to the exercise. The amount of the loan is going to be important as a higher principle on the loan has a higher risk of being paid back. A high interest rate means a higher debt servicing cost and a lower income comperative income would also increase the risk. Lastly, the total amount of debt and number of accounts is important as additional debt means addition debt servicing costs apart from the loan being extended, and would therefore mean a higher risk of the borrower is in a lot of debt. Derogatory marks are negative past behaviors in relation to credit, such as delinquent payments, bankruptcies, etc.


The process for machine learning began by importing all of the necessary dependencies from sklearn. Then I read in the csv into the jupyter lab file. At this point I isolated the "loan status" column in variable 'y' which served as my labels. The rest of the columns were uploaded into variable 'x', serving as the features which the model would use to predict the loan status. At that point the data was split using train_test_split, fit into a Logistic Regression model, and created the predictions. The last step was to print the training report to see the results of the model.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
 - balanced_accuracy_score = 0.95
 
 - "0" - healthy loan
    - precision = 1.00
    - recall = 1.00
    - f1-score = 1.00
    - support = 56271
    
- "1" - high risk loan
    - precision = 0.86
    - recall = 0.90
    - f1-score = 0.88
    - support = 1881

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
Model 1 performed well. The perfect precision and recall scores indicate that the model is good at predicting the the healthy loans. However, the model was somewhat worse at predicting the high risk loans, indicating that the model had a proclivity to label loans as healthy. The issue with banking is that bad loans have to be made up using interest payments from healthy loans. Single digit interests on loans means that a significant number of healthy loans are required to make up for delinquent loans. A bank would prefer a delinquency rate lower than 2-3% in order to maintain a healthy portofolio. For that reason, as strong as the model is, it might not be adquate for a bank to use. 
