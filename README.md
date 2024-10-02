# credit-risk-classification
## Overview of the Analysis
The purpose of this analysis was to build a logistic regression machine learning model to predict whether any given borrower will default on a loan that they have taken out, using information related to their borrowing history. The model was built using the borrowing history of a set of borrowers supplied by a lending company.The model was built using the features associated with the borrowing histories of a set of borrowers provided by a lending company. These features were loan size, interest rate, income, debt, debt-to-income ratio, number of accounts, and derogatory marks. The feature, number of accounts seems to refer to accounts which contain the liquid assets of the borrowers. It was unclear to me what the feature, derogatory marks means, but if I were to guess, this feature, for a borrower, is a tally of instances in which the borrower exhibited poor behavior relevant to the loan. The variable which I wished to predict using the model, was loan status. Loan status, with 2 possible values of 0 and 1, means healthy loan or at-risk loan, respectively. Preprocessing involved checking the data types of each of the features/columns to make sure none of the data types needed to be changed and checking for missing values. Next, I used SciKit Learn's method for splitting the data into training and testing data to see how reliable the model was and to avoid overfitting the model to the training data. The default training-to-testing split ratio of SciKit-Learn's method for splitting the data into training and testing components is 0.75/0.25. After splitting the data, I fit the logistic regression model on the training data via SciKit-Learn's logistic regression method and used the model to generate predicted loan results for the testing data. Finally, utilizing SciKit-Learn again, I generated a confusion matrix and classification report to evaluate the accuracy, recall, and precision of the model on the testing data. 
## Results
    * Accuracy: 99%
    * Precision:
        * Healthy Loans: 100% (Rate at which actual healthy   loans are predicted to be healthy out of all the predicted healthy loans)
        * At-Risk Loans: 85% (Rate at which actual at-risk loans are predicted to be at-risk out of all the predicted at-risk loans)
    * Recall:
        * Healthy Loans: 99% (Rate at which actual healthy loans are predicted healthy out of all actual healthy laons)
        * At-Risk Loans: 91% 
        (Rate at which actual at-risk loans are predicted at-risk out of all actual at-risk loans)
## Summary
The evaluation of this performance depends on the financial context of this situation. In this situation, it depends on whether the company wants to be liberal or conservative in their approach. Since the impact of a loan defaulting could be devastating, since only 91% of actual at-risk loans are accurately predicted to be to be at-risk, I would argue that a logistic regression model may not be the best model for the data at hand. If I had more time, I would fit other supervised machine learning models, such as SVM, decision trees, random tree forests, and neural networks, and compare the results to the results of the logistic regression model. 
