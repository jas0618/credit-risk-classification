# credit-risk-classification Report 

 ## Analysis 
The purpose of this analysis is to identify borrowers who are more likely to default on their payments by examining key variables such as income, interest rate, number of existing accounts, and debt relative to income. The goal of the lending service is to assess creditworthiness using these factors to determine whether a borrower is in a stable financial position or poses a high risk if granted a loan.
The financial information included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, and total debt. The key variables required for the analysis are current interest rates, borrower income, debt-to-income ratios, and total debt. The X_train, X_test, Y_train and Y_test using the logistic regression model. 


# Stages of Machine Learning
  
1. Split the Data into Training and Testing Sets
Use the train_test_split module to divide the dataset into training and testing sets.
Define X_train, X_test (independent variables) and y_train, y_test (dependent variable) to ensure the model can learn patterns from historical data while being tested on unseen data.

2.Initialize and Train the Logistic Regression Model

Set up the logistic regression model using random_state=1 to ensure reproducibility.
Train the model using X_train and y_train, allowing it to learn the relationship between borrower attributes and loan default risk.

3.Generate Predictions for Loan Default Probability

Apply the trained model to X_test using the .predict() function.
Create a results dataframe with two columns: Predicted Loan Default Status and Actual Loan Default Status to compare the model's output with real outcomes.

4.Evaluate Model Performance with a Confusion Matrix

Generate a confusion matrix to assess how well the logistic regression model differentiates between healthy loans and high-risk loans.
The confusion matrix provides insight into true positives, false positives, true negatives, and false negatives, helping to identify areas for model improvement.

5.Assess Model Accuracy Using Key Performance Metrics

Evaluate the model using precision, recall, and F1-score:
Precision: Measures how many predicted defaults were actually defaults.
Recall: Assesses how many actual defaults were correctly identified.
F1-score: Balances precision and recall, ensuring a well-rounded evaluation.
These metrics help determine whether the model effectively identifies high-risk borrowers while minimizing misclassification.

Logistic Regression (LogisticRegression):

Used as the primary classification algorithm to predict whether a borrower is likely to default on their loan.
This model is well-suited for binary classification problems, making it effective in distinguishing between high-risk and healthy loans based on borrower attributes.

Train-Test Split (train_test_split):

Utilized to divide the dataset into training and testing sets.
Ensures that the model is trained on one portion of the data while being evaluated on unseen data, preventing overfitting and improving generalization.


Confusion Matrix (confusion_matrix):

Used to assess the model's performance by comparing predicted and actual loan default outcomes.
Provides key metrics such as true positives, false positives, true negatives, and false negatives, helping to evaluate the model’s effectiveness in identifying risky borrowers.

## Results 

# Accuracy Scores
Measures the overall correctness of the model.
Formula:
Accuracy= 
TP+TN/
+FP+FN+TP+TN
​ 
Limitations:
Can be misleading if there is class imbalance.
A model predicting all negatives in a rare event (e.g., fraud detection) may have high accuracy but poor performance.

# Precision
Measures the proportion of correctly predicted positive cases out of total predicted positives.
Formula:
Precision= 
TP/FP+TP
​ 
Best for:
Cases where false positives are costly (e.g., medical diagnosis, spam detection).

# Recall Scores 
Measures the proportion of actual positive cases that were correctly predicted.
Formula:
Recall= 
TP/FN +TP
​
Best for:
Cases where false negatives are costly (e.g., fraud detection, disease screening).

* Machine Learning Model 1:
*  Accuracy, Precision, and Recall scores.
  # Answer:
The precision score, accuracy and recall scores for healthy loans was 100%, the logistic regression model had no errors or missed data points or false negatives
The precison socre, accuracy and recall score for high- risk loans was 91%, the logistic regression model had missed data points and false negatives 

## Summary 

Based on the evaluation metrics, the Neural Networks model demonstrated the highest performance.
It achieved superior recall and precision, ensuring that it correctly identified borrowers who are at risk of default while minimizing false positives.
Neural networks are highly effective for large datasets, capturing complex relationships that traditional models like Logistic Regression may overlook.

Although Logistic Regression is a strong choice for simple binary classification tasks such as this one and works well with smaller datasets, it may struggle with non-linear patterns in borrower risk assessment.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
# Answer 
Yes, the choice of the best model depends on the business objective.
For loan default prediction, recall is typically more important, as missing a high-risk borrower could result in financial loss for lenders.
   

If you do not recommend any of the models, please justify your reasoning:

Neural Networks is the preferred model for this problem due to its higher accuracy, recall, and precision, making it well-suited for complex borrower assessment.
If the dataset were smaller or more interpretable results were required, Logistic Regression could be a viable alternative.


