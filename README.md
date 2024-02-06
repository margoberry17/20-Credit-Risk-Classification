# 20-Credit-Risk-Classification
Supervised Machine Learning

## Background
Used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Split the Data into Training and Testing Sets

- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

![01 Lending Data](https://github.com/margoberry17/20-Credit-Risk-Classification/assets/136475202/b11c3482-7846-4de0-b28d-912fc5553142)


- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
- Split the data into training and testing datasets by using train_test_split.


## Created a Logistic Regression Model with the Original Data

- Fit a logistic regression model by using the training data (X_train and y_train).
- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
- Evaluate the model’s performance by doing the following:
    - The Testing Accuracy with the original data is: 0.967989851522121
    - Generate a confusion matrix.

    ![Confusion testing](https://github.com/margoberry17/20-Credit-Risk-Classification/assets/136475202/1485a5dd-5535-477b-b6af-d8f41d9c7e7d)

      
    - Print the classification report.
 
    ![CR - testing](https://github.com/margoberry17/20-Credit-Risk-Classification/assets/136475202/2e8d4bbd-a490-4b10-9f10-ceac61209ead)
     

- How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
For healthy loans ('0') the percision is 100%, the recall is 99%, and the f1-score is 100%, meaning that the model does really well when perdicting instances. For high-risk loans ('1') the percision is 85%, the recall is 91%, and the f1-score is 88%, meaning that the model does moderately well in predicting instances. It predicts Actual Healthy Loans really well, but 36 loans were "False Positives," meaning they were high risk loans but predicted as healthy.  

## Created a Logistic Regression Model with the Resampled Training Data

- Fit a logistic regression model by using the training data (X_resampled and y_resampled).
- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
- Evaluate the model’s performance by doing the following:
    - The Testing Accuracy with the resampled data is: 0.9935981855334257
    - Generate a confusion matrix.

    ![Confusion oversampled](https://github.com/margoberry17/20-Credit-Risk-Classification/assets/136475202/54d78279-a67d-4768-b703-21dc07382d16)


    - Print the classification report.
 
    ![CR oversampled](https://github.com/margoberry17/20-Credit-Risk-Classification/assets/136475202/b872a684-e750-4490-b2da-b007ad3fb6e6)


- How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Credit Risk Analysis Report
- An overview of the analysis: Explain the purpose of this analysis.
- The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
- A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

The oversampled data generated an accuracy score of 99% which turned out to be slightly higher than the original model (97%). The oversampled model performs better since it limited labeling the amount of non-healthy (high-risk) loans as healthy (low-risk). A lending company would want to go with the oversampled model since it would be more costly for a lending company to identify non-healthy loans as healthy due to loss of funds, where as healthy loans being identified as non-healthy is not ideal but safer due to no loss in terms of money. 
