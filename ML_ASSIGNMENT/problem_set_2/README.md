Problem Set 02: Predicting Term Deposits with Logistic Regression.

# Problem Statement
A bank wants to anticipate whether a customer would open a term deposit based on demographic and financial information. The challenge involves creating a Logistic Regression model for classification.

# Dataset: Bank Marketing dataset.  
Contains 17 variables, including client demographics, account information, and subscription status (yes/no).

# Approach.
A Logistic Regression classification approach was used to predict customer subscriptions.

The methodology is as follows:

## Data Preprocessing.
- Handled any missing values.
- Converted category variables with encoding
- Feature scaling is implemented if necessary.
- Engineered features, such as handling pdays.

## Model Building
- A Logistic Regression model was utilized.
- Target variable: subscription (yes or no)

### Training
- Data split into training and testing sets
- Model trained on training data

## Evaluation
- Accuracy score calculated
- Confusion matrix used
- Classification report (precision, recall, F1-score)

## Findings
- Model was able to predict customer behavior reasonably well
- Certain features had strong influence on prediction
- Performance can improve with feature selection and tuning

## Conclusion
Logistic Regression provides a simple yet effective baseline model for customer subscription prediction.