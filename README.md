# credit-risk-classification

PURPOSE OF ANALYSIS:
The purpose of this analysis is to build and evaluate machine learning models to predict loan status (fraudulent or legitimate) based on financial features.

DATASET INFO:
The dataset contains financial information for loan applications, including features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt and loan status.The target variable is the loan status, where 0 represents legitimate loans and 1 represents fraudulent loans.

MODEL TRAINING AND ANALYSIS:
Logistic Regression without Resampling
    - Balanced Accuracy Score: 0.952
    - Confusion Matrix: [[18663,   102],
                        [   56,   563]]
    - Classification Report:  precision    recall  f1-score   support

                            0       1.00      0.99      1.00     18765
                            1       0.85      0.91      0.88       619
                        accuracy                        0.99     19384
                        macro avg    0.92      0.95     0.94     19384
                        weighted avg 0.99      0.99     0.99     19384

Logistic Regression with Resampling
    - Balanced Accuracy Score: 0.994
    - Confusion Matrix: [[18649, 116],
                        [ 4, 615]]
    - Classification Report:  precision    recall  f1-score   support

                            0       1.00      0.99      1.00     18765
                            1       0.84      0.99      0.91       619

                        accuracy                         0.99     19384
                        macro avg    0.92      0.99      0.95     19384
                        weighted avg 0.99      0.99      0.99     19384
                        
SUMMARY:
In this analysis, we trained and evaluated two Logistic Regression models for predicting loan status based on financial features. The model trained with random over-sampling achieved a higher balanced accuracy (0.994) compared to the model without resampling (0.952). Additionally, the recall for fraudulent loans (class '1') improved significantly with random over-sampling (0.99) compared to the non-resampled model (0.91) while the recall for non-fraudulent loans (class '0') remained consistant in both regression models (0.99) .
Considering the balanced accuracy, precision, and recall scores, the Logistic Regression model with random over-sampling is recommended for predicting loan status in this dataset as the overall accuracy is higher. 

The choice of model really depends on the business context and the trade-off between different evaluation metrics. If the focus is strictly on accurately detecting fraudulent cases, the model with random over-sampling is the preferable choice as it is more accurate during this set of testing.