## Overview
Credit card fraud is a type of financial crime where a criminal uses a stolen or fake credit card to make unauthorized purchases. This is a growing problem as the use of credit cards has increased in recent years. The problem with credit card fraud is that it can result in significant financial losses for both the credit card holder and the bank issuing the card.

It is important to detect credit card fraud because it helps to minimize the financial losses that can result from this type of crime. By detecting fraudulent transactions early, banks can prevent the unauthorized use of credit cards and reduce the impact of fraud on their customers. Additionally, early detection of fraud can also help to reduce the time and resources required to resolve fraudulent activities, making the process more efficient for all parties involved.

Overall, detecting credit card fraud is crucial for maintaining the integrity of the financial system and protecting the interests of both consumers and banks. Machine learning algorithms can play a key role in detecting fraud by analyzing large amounts of data to identify patterns and anomalies that may indicate fraudulent activity.

## Business and Data Understanding
The target audience for a credit card fraud detection project would likely include several key stakeholders, including:

* Banks and financial institutions: These organizations are likely to be interested in this solution as they bear the financial burden of credit card fraud. By detecting fraud early, banks can reduce their losses and improve the security of their customers' financial information.

* Credit card issuers: Companies that issue credit cards also have a vested interest in reducing fraud, as this helps to protect their reputation and brand image. They may be interested in a solution that helps them to quickly identify and prevent fraudulent transactions.

* Consumers: Credit card holders are often the primary victims of credit card fraud, so they would be interested in a solution that helps to prevent unauthorized transactions and protect their financial information.

* Regulatory agencies: Governments and regulatory bodies may also be interested in this solution as it helps to reduce the financial losses and consumer harm associated with credit card fraud. This can help to maintain the stability and security of the financial system as a whole.

Data used was collected from:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
Data contained 284807 rows and 31 columns.
Dataset had no missing values but was highly unbalanced between the fraudulent and non-fraudulent dataset.
I separated the fraudulent and non-fraudulent data then later sampled from the non-fraudulent dataset.
I split the data into features and targets then  later used 25% of the data as the test size.

## Modeling
Modelled using:
* Logistic Regression
* KNN Classifier
* Random Forest
* SVC Model
* Random Forest with tuned hyperparameters

## Evaluation
1) Logistic Regression
The model had an accuracy of 93.77% on the training data and 93.50% on the test data.
Precision of 0.983. This indicates that the model is making fewer false positive predictions i.e. fewer cases of fraud are being classified as non-fraud.
Recall: 0.906. This indicates that the model identified most of the fraud cases.
F1 score.0.943. Indicates model has a good balance between precision and recall

2) KNN Classifier
The model had an accuracy of 76.42% on the training data and 62.20% on the test data.
Precision: 0.642 
Recall: 0.617
F1 score: 0.630

3) Random Forest
The model had an accuracy 94.71% on the test data.
Precision: 0.975. Model is making fewer false positive predictions
Recall: 0.922. The model is able to identify most of the fraud cases
F1 score: 0.948. Model has a good balance between precision and recall

4) SVC Model
Precision: 1.0 
Recall: 0.852 
F1 score: 0.919 

5) Random Forest with tuned Hyperparameters
Best parameters found: {'max_depth': 20, 'min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 50} - This is the set of hyperparameters that result in the best performance for the Random Forest model, as determined by the grid search or other hyperparameter tuning method used.
Best score found: 0.93698850098415 - This is the highest accuracy, F1-score, or other performance metric that was obtained during the hyperparameter tuning process. In this case, the score is 0.9369, which is a good score and suggests that the Random Forest model is performing well for the credit card fraud detection task.

## Conclusion
I found random forest to be the best Ml model for this dataset. Use of this model may lead to reduce in financial losses associated with credit card fraud and improving the security of customer financial information