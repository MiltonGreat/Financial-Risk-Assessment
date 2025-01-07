# Financial-Risk-Assessment-Machine-Learning-Model

### Overview

This project explores and develops a machine learning pipeline to predict loan approvals based on customer financial and demographic data. The pipeline involves data cleaning, feature engineering, exploratory data analysis, and classification model training and evaluation.

### Objectives

The goal of this project is to analyze and predict loan approvals while assessing financial risks associated with borrowers. This involves creating a classification model that predicts whether a loan will be approved (binary classification). Key objectives include:

- Clean and preprocess financial and demographic data.
- Engineer meaningful features for better predictive performance.
- Train and evaluate machine learning models.
- Interpret the results to support decision-making in financial risk management.

### Dataset

The dataset includes customer financial data such as annual income, monthly debt payments, credit history, and other demographic information.

### Pipeline

##### Data Preprocessing
- Handled missing values by filling numerical columns with median values and categorical columns with mode.
- Converted date columns into meaningful numeric features (e.g., year, month).
- One-hot encoded categorical variables.
- Standardized numerical features using StandardScaler.

#### Feature Engineering

Created new features such as:
- DebtToIncomeRatio: Ratio of monthly debt payments to annual income.
- NetWorth: Total assets minus total liabilities.

Model Training
- Split the data into training (80%) and testing (20%) sets.
- Trained a Random Forest Classifier with balanced class weights to handle class imbalance.

Model Evaluation
- Evaluated the model using metrics:
- Accuracy: 92.33%

### Results

- Accuracy	92.33%
- Precision (0)	93%
- Precision (1)	91%
- Recall (0)	97%
- Recall (1)	78%
- F1-score (0)	95%
- F1-score (1)	84%

### Key Insights

- High precision for approved loans (1), making the model suitable for reducing false positives in financial risk assessment.
- High recall for non-approved loans (0), ensuring fewer risky approvals.
- The DebtToIncomeRatio and NetWorth were significant features influencing loan approval predictions.

### Source

https://www.kaggle.com/c/GiveMeSomeCredit
