# 20-Credit-Risk-Classification
Supervised Machine Learning

## Background
Used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Split the Data into Training and Testing Sets

- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
- Split the data into training and testing datasets by using train_test_split.


## Created a Logistic Regression Model with the Original Data

- Fit a logistic regression model by using the training data (X_train and y_train).
- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
- Evaluate the model’s performance by doing the following:
    - Generate a confusion matrix.
    - Print the classification report.

- How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?


## Credit Risk Analysis Report

- An overview of the analysis: Explain the purpose of this analysis.

- The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

- A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
