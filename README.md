# Loan_Outcome_Prediction_with_Logistic_Regression
# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to predict accurately both the risky loans and healthy loans.

The model uses the following features to predict the loan outcome.
*loan_size
*interest_rate
*borrower_income
*debt_to_income
*num_of_accounts
*derogatory_marks
*total_debt

The data hold 75036 healthy loans and 2500 risky loans data. This is considered to be imbalanced data.

The workflow of the analysis as follows:

*Splited the data using train_test_split and defined the random state.
*Scaled the features for test and training data using Standars Scaler as the features have wide range of numerical values.
*Built the logistic regression model,fitted the data, and predicted the loan outcome.
*Measured the model performance using balanced accuracy score, confusion matrix and classification_report.

The model was built using Logistic Regression. The model predicted the results both on original data and resampled the data (using the resampling algorith and created the same number of results for healthy and risky loans (56271 each).

## Results

* Machine Learning Model 1 (original scaled data):
  balanced_accuracy_score: 0.9889115309798473
  ![Screen Shot 2023-03-26 at 1 50 04 PM](https://user-images.githubusercontent.com/113545468/227794451-8e4642bd-57b1-4809-ba92-08d6bfcadcff.png)
  ![Screen Shot 2023-03-26 at 1 50 08 PM](https://user-images.githubusercontent.com/113545468/227794455-1125203f-3ba0-4a15-9a62-09297dfe1c7e.png)

* Machine Learning Model 2(resampled data):
  balanced_accuracy_score:0.9933850227303349
  ![Screen Shot 2023-03-26 at 1 48 30 PM](https://user-images.githubusercontent.com/113545468/227794392-da7662aa-d085-4116-84e6-310f9771ca91.png)
  ![Screen Shot 2023-03-26 at 1 48 37 PM](https://user-images.githubusercontent.com/113545468/227794403-da00189e-403e-46f2-b20a-d91256cc520f.png)

 

## Summary


Based on the both results, I consider the both model perform satisfactory and can move to the production since the both accuracy scores are 0.99 which is extremely high. However, from the business stand point, every false positives (FP) will be lost opportunity for the bank and every false negative (FN) will be loss for the bank as the loan would not get paid back. Therefore, it is equally important to predict both `1`'s and `0`'s. The first model have 7 more FPs and 6 less FNs than the second model. Overall, it cancels each other. Therefore, I recommend the both models and they perform very similar.


