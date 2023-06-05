## Overview of the Analysis

The project is aimed at using ML to analyse historical activity from a lending company and create a model that weighs up the loan risk of applicants that are borrowing credit.

By fitting an ML model to the loan status data I determine the credibility of loan appplications - i.e those that are low risk, and those that are high risk for the lending company.

**Some Key Steps**
- First I split the data into training and testing datasets by using 'train_test_split'
- Then I used the 'value.counts' function to check the balance of the data, which showed a great imbalance
- I then used the RandomOverSampler module from the imbalanced-learn library to resample the data and adjust the imbalance in the target values
- I then fitted the Logistic Regression model to orginal data and the resampled data and created accuracy reports for each

<img width="467" alt="Screenshot 2023-03-27 at 11 05 27" src="https://user-images.githubusercontent.com/115706722/227917531-801104b2-4fda-4083-a986-bccf4db21731.png">

## Results

* Machine Learning Model 1: Original Data

<img width="440" alt="Screenshot 2023-03-27 at 11 28 47" src="https://user-images.githubusercontent.com/115706722/227916432-5156fe20-b50f-481a-a302-fbce68fcafe8.png">


* Machine Learning Model 2: Resampled Data

<img width="422" alt="Screenshot 2023-03-27 at 11 29 00" src="https://user-images.githubusercontent.com/115706722/227916484-2f6943af-c16f-427e-a556-4e138b108185.png">

## Analysis

These reports show that by fitting the logistic regression model to the original data provided by the lending company, there is a cosniderable difference in recall scores. The difference in recall values between healthy (non-risky) loans, row '0' and un-healthy (risky) loans, row '1' indicates that the model will better predict unrisky loans than risky loans, which is not suitable for the context of our project.


## Summary


The performance of the logistic regression model with the resampled, balanced data is strong, increasing the original data accuracy score from 0.952 to 0.993 and the recall prediction for the high risk applicants from 0.91 to 0.99. This is very important for so the model does not label non-healthy, high risk applicants as low risk for approval.

Using imbalanced data in the model runs a far greater risk of wrongly classifying data. For example, classifying a low risk, safe loan as a risky loan, or more crucuially, classifying a high risk loan as a safe loan to be approved. The latter is known as a false positive.

The confusion matrix shows a considerable decrease in the number of false positive results, which reflects a correct classification of applicants and loan data. For this reason I would reccomend the second model in this analysis, a Logistic Regression model fitted with balanced, oversampled data.

