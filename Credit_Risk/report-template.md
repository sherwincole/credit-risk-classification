# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
    We are looking to build a tool that helps us perdict and identify healty loans vs high-risk loans.

* Explain what financial information the data was on, and what you needed to predict.
    Loan size, interest rate, borrower income, debt to income, nummber of accounts, derogatory marks, total debt, and loan status.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    We used total loan counts or loan_status, Length: 77536, and then our data given in the CSV like Loan size, interest rate, borrower income, debt to income, nummber of accounts, derogatory marks, total debt.

* Describe the stages of the machine learning process you went through as part of this analysis.
    * Splitting data into labels and features, with the loan status (healthy or high-risk) being the label and the remaining seven columns as features.
    * The data was then split into training and testing data sets.
    * A Logistic Regression model from sklearn was created.
    * Logistic Regression as a binary classifier was chosen as we are classifying loans as healthy OR high-risk and only those two options.
    * The model was then fit with the training data.
    * Predictions were made with the test data.
    * The model’s performance was evaluated using accuracy, precision, and recall scores.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
    We used a Logistic Regression model from sklearn to complete this module. 

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.
* Machine Learning Model 1:
    * Accuracy: The overall accuracy of the model is 0.99, indicating that it correctly classifies 99% of the instances.

    Precision

    * Healthy Loan (class 0): 1.00
    * High-Risk Loan (class 1): 0.84

    Recall

    * Healthy Loan (class 0): 0.99
    * High-Risk Loan (class 1): 0.94

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.



The logistic regression model performs very well in predicting healthy loans (class 0), with a precision of 1.00 and a recall of 0.99. For risky loans (class 1), the model still shows strong performance, achieving a precision of 0.84 and a recall of 0.94.

The slightly lower precision and recall for class 1 may be due to the class imbalance in the dataset—only 619 test samples are labeled as class 1, compared to 18,765 for class 0. This imbalance limits the model’s ability to learn patterns associated with high-risk loans. Adding more examples of risky loans to the training data could help improve its performance in this area.

When classifying loans, it's especially important to identify high-risk loans accurately, as a single default can result in greater financial loss than the profit gained from several low-risk loans. Overall, the model achieves a high accuracy of 99%.
