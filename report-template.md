# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to build a machine learning model that can predict the creditworthiness of borrowers in a peer-to-peer lending service. Specifically, the goal is to classify loans as either **healthy (0)** or **high-risk (1)** based on a variety of financial indicators provided in the dataset.

The dataset contains information on different loan characteristics, and the target variable is `loan_status`:
- **Healthy Loan (`0`)**: Indicates the loan is likely to be paid back without issues.
- **High-Risk Loan (`1`)**: Indicates the loan has a higher chance of defaulting.

Stages of the machine learning process in this analysis include:
1. **Loading and preparing the data**: Separating the features (X) and labels (y).
2. **Splitting the data**: Using `train_test_split` to create training and testing sets.
3. **Training the model**: Applying the `LogisticRegression` algorithm.
4. **Evaluating the model**: Generating a confusion matrix and classification report to assess performance.

---

## Results

### Machine Learning Model: Logistic Regression
- **Accuracy**: 99%  
  - The model accurately classifies 99% of the loans in the dataset.
- **Precision**:  
  - **Healthy Loans (0)**: 1.00  
  - **High-Risk Loans (1)**: 0.86  
  - The model achieves perfect precision for healthy loans, meaning no high-risk loans are incorrectly labeled as healthy.
- **Recall**:  
  - **Healthy Loans (0)**: 0.99  
  - **High-Risk Loans (1)**: 0.94  
  - The model identifies 94% of actual high-risk loans, meaning only 6% are missed.

---

## Summary

The logistic regression model performs extremely well, achieving high accuracy, precision, and recall scores. Given the results:
- **Healthy Loans (0)** are identified with near-perfect precision and recall.
- **High-Risk Loans (1)** are also predicted with high recall (0.94), meaning the model detects most risky loans, which is crucial for reducing potential financial losses.

### **Recommendation**
The model can be confidently recommended for use by the company. It performs well across all key metrics, especially in identifying high-risk loans, which is typically the main focus in credit risk prediction.

- **If the company prioritizes minimizing missed high-risk loans (false negatives)**, further improvements (such as adjusting thresholds or using class weights) could slightly enhance recall. However, the current performance is already strong.

This logistic regression model balances **accurate detection of high-risk loans** with **minimizing false positives**, making it suitable for deployment in the credit risk assessment process.

