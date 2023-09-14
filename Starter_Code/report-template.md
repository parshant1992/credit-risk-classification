## Overview of the Analysis

The purpose of this analysis is to develop machine learning models to predict the loan status (either healthy or high-risk) based on financial information provided in the dataset. The dataset contains various features related to loan applications, and we aim to predict whether a loan will be healthy (0) or high-risk (1).

Key points regarding the analysis:

- **Financial Information**: The data includes financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status.

- **Prediction Target**: We are trying to predict the "loan_status" variable, which is binary, with "0" indicating a healthy loan and "1" indicating a high-risk loan.

- **Stages of Machine Learning Process**: The analysis follows these stages:
  1. Data Preparation: Reading the dataset, splitting it into training and testing sets, and checking the balance of the target variable.
  2. Model Building: Creating a Logistic Regression model with the original data and evaluating its performance.
  3. Resampling: Using RandomOverSampler to address class imbalance and creating a Logistic Regression model with resampled data.
  4. Model Evaluation: Assessing model performance through accuracy, precision, and recall metrics.

- **Methods Used**: Logistic Regression is employed as the primary classification algorithm. Additionally, oversampling using the RandomOverSampler method from the imbalanced-learn library is applied to address class imbalance.

## Results

### Machine Learning Model 1 (Logistic Regression with Original Data):

- Balanced Accuracy Score: 99%
- Precision and Recall:
  - Class Purple (Healthy Loan):
    - Precision: 100%
    - Recall: 99%
  - Class Yellow (High-Risk Loan):
    - Precision: 85%
    - Recall: 91%

### Machine Learning Model 2 (Logistic Regression with Resampled Data):

- Balanced Accuracy Score: 99%
- Precision and Recall:
  - Class Purple (Healthy Loan):
    - Precision: 100%
    - Recall: 99%
  - Class Yellow (High-Risk Loan):
    - Precision: 84%
    - Recall: 99%

## Summary

Both machine learning models perform exceptionally well in predicting loan status. Here's a summary of the key points:

- **Performance**: Both models achieve a balanced accuracy score of 99%, indicating a strong overall ability to predict both healthy and high-risk loans.

- **Class Imbalance**: Model 2, which utilizes oversampled data, effectively addresses class imbalance and maintains high precision and recall for high-risk loans.

- **Recommendation**: Model 2, trained with oversampled data, is recommended for its balanced performance in predicting both healthy and high-risk loans. This model is especially suitable if high-risk loan prediction is of particular importance. However, Model 1 is also highly accurate and may be sufficient if class imbalance is not a critical concern.

The choice between the models may depend on the specific business goals and the relative importance of correctly predicting healthy and high-risk loans.