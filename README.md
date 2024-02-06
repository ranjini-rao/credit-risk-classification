# credit-risk-classification
Module 20 Challenge
# Overview of the Analysis
- The purpose of this activity is to analyze a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
- Financial information present on the data for prediction are #loan_size #borrower_income #debt_to_income #derogatory_marks #loan_status
- Target value count gives us the information on dataset where 0-value count of 75036 indicating loan is healthy and value of 1-value count of 2500 making these high risk loans.
- The stages of the machine learning process went through as part of this analysis are Creating label sets, training and recognizing the pattern by using train_test_split, validating and evaluating the model by calculating accuracy scores, confusion matrix, and classification report.
- Uilizing the supervised learning classification model called Logistic Regression to predict the probability of the healthy loans vs high-risk loans. Since the data highly targetted towards the healthy loans, RandomOverSampler was used to reduce the imbalances and LogisticRegression was then applied to the oversampled data.
# Results
Machine Learning Model 1 - Logistic Regression
- Accuracy: The model displays 18663 true positive results and 563 true negative results. This model does a good job in predicting both the healthy and the high-risk loans as can be inferred from the balanced accuracy score of 95.20%
- Precision: The model performs better predicting healthy loans (precision 1) than high-risk loans (precision 0.85). The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 85% of the times.
- Recall scores: The model performs better predicting healthy loans (recall 0.99) than high-risk loans (recall 0.91). The scores imply that for all the instances where the loans were actually healthy, 99% of the times they were classified correctly. However, for all the instances where the loans were actually high-risk, they were classified correctly 91% of the times.
  
Machine Learning Model 2 - RandomOverSampler:
- Accuracy: The model displays 56271 true positive results and 56271 true negative results. The model does a great job in predicting both the healthy and the high-risk loans as can be inferred from the balanced accuracy score of 99.36%

- Precision: The model performs well for predicting healthy loans (precision 1) and high-risk loans (precision 0.84). The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 84% of the times.

- Recall: The model performs equally well for predicting healthy loans (recall 0.99) and high-risk loans (recall 0.99). The scores imply that for all the instances where the loans were actually healthy or when they were high-risk, 99% of the times they were classified correctly.

# Summary
The RandomOverSampler model outperforms the logistic regression model applied to oversampled data, exhibiting balanced accuracy scores. The RandomOverSampler technique proves effective in accurately predicting loans, particularly high-risk ones ('1'), and maintaining strong performance for healthy loans ('0'). Identifying high-risk loans is crucial for lending companies, as it minimizes the risk of defaulters and positively influences overall profitability through accurate creditworthiness analysis. The RandomOverSampler model excels in correctly classifying high-risk loans, significantly reducing mislabeling errors. Considering these factors, the recommended approach involves employing the RandomOverSampler method to rebalance the data, with a focus on overweighting healthy loans, followed by logistic regression. This method yields superior accuracy and recall scores, essential decision metrics for lending service companies.






