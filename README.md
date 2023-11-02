# credit-risk-classification
## Overview
The purpose of this Challenge was to use several techniques to train and evaluate data for loan risk. The lending_data.csv showed the size of the loan, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and loan status for each applicant. The techniques utilized were ways for a computer to determine who should be approved for a loan based on the risk of them defaulting on the loan (high-risk) and the likelihood of them paying their loan in full by the end of the loan (healthy loan). The variable I was trying to predict was the loan status and how well the models predict both the 0 (healthy loan) and 1 (high-risk loan) labels. 

Once the predicting target variable (labels) was selected, I was then able to separate the data based on labels and features (the independent variables used by the machine learning model to make predictions about the labels). I then used the sklearn.model_selection to test_train_split the data. In other words, it split my data into two sets; one to train the model so that it knew what independent variables were influencing the predicting target variable by analyzing patterns and relationships. The computer then used the other dataset (test) to apply what it learned during training to predict the future. Basically the test_train_split function does the splitting then I utilized the Logistic Regression Model to train and test the data and then created a confusion matrix and classification report to analyze the model's performance.

## Results
* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
The logistic regression model predicted healthy loans very well and reasonably well predicting high risk loans. The model had all instances of predicted healthy loans correct and captured 99% of the actual healthy loans. However, only 85% of the predicted high risk loans were correct and the model captured 91% of the high risk loans. The F1-score, which gives a score that gives equal weight to both the precision and accuracy scores, is 1.0 for healthy loans and 0.88 for high-risk loans. The macro average, which treats all classes equally, for the f1 was .94 and the weighted average (formula that accounts for class imbalances) was .99.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
The logistic regression model fits exceptionally well with the oversampled data when predicting healthy loans and good at predicting high-risk loans. For the accuracy of the models' accurate positive predictions, the healthy loans were all correct and 84%  of the high-risk loans were correct. However, the model correctly identified 99% of both health and high-risk loans This gives a 1.00 F1-score for healthy loans and 0.91 for high-risk loans which are both a great balance between precision and recall. The overal accuracy is 99% which suggest the model is accurate and efficient. The macro average was .95 and the weighted average was .99.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

I recommend the Machine Learning Model 2 because in Model 1, there was a class imbalance in the dataset (more 0/healthy loans, than 1/high-risk loans). The Random OverSampling in Model 2 helped balance the class distribution by creating additional samples in the minority class (in this case, the 1s). In turn, this made Model 2 more efficient. It is more important to accurately predict the 1s (high-risk loans) because these are the loans that will cost the lenders. However, they also want to accurately predict the 0's since they also make them the money on the interests of the loans. Model 2 also has a higher F1 score than Model 1, which gives equal weight to both the precision and recall and therefor, more precise than looking at precision or recall on their own.

## Reference
I utilized ChatGPT to help complete this project in a timely and efficient manner. 
