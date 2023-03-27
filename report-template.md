# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).


* Overview of the Analysis

The project is aimed at using ML to analyse historical lending activity from a lending company and create a model that weighs up the risk of applicants that are borrowing credit.

By fitting an ML model to the loan status data I determine the credibility of loan appplications - i.e those that are low risk, and those that are high risk for the lending company.

This project uses logistric regression algorythem 

First I plit the data into training and testing datasets by using 'train_test_split'
The imbalance in the dataset beween risky and safe loans was great, which would cause a clear bias in the model

Using the dataset provided by the lending company, I created a Logistic Regression Model that generated an accuracy score of 95%. Although the model generated a high-accuracy, the models recall value (0.91) for non-healthy loans is lower than the recall value (0.99) for healthy loans. This indicates that the model will predict loan status's as healthy better than being able to predict loan status's as non-healthy. This is due to the dataset being imbalanced, meaning that most of the data belongs to one class label (in this case healthy loans greatly outweighed non-healthy loans).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )



Using imbalanced in the model runs a far greater risk of wrongly classifying data. For example, classifying a low risk, safe loan as a risky loan, or more crucuially, classifying a high risk loan as a safe loan to be approved.

 How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

The performance of the logistic regression model with the balanced data is strong, increasing the accuracy score from 0.952 to 0.993 and the recall prediction for the high risk customers from 0.91 to 0.99, which is very important for not approving high risk applications.

 I created a Logistic Regression Model fit with the oversampled data that generated an accuracy score of 99%, which turns out to be higher than the model fitted with imbalanced data. The oversampled model performs better due to the dataset being balanced. The models non-healthy loans recall value increased from 0.91 to 0.99 indicating that the model does an exceptional job in catching mistakes such as labeling non-healthy (high-risk) loans as healthy (low-risk).