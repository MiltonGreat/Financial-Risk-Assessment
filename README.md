# Financial-Risk-Assessment-Machine-Learning-Model

### Overview

This project aims to enhance loan approval processes by developing a machine learning model that predicts loan approvals while ensuring fairness and transparency. By leveraging the "Give Me Some Credit" dataset, the model analyzes financial and demographic data to assess credit risk, balancing high predictive accuracy with ethical fairness standards.

### Problem Statement

Loan approval decisions can significantly impact individuals and businesses, but traditional credit scoring models often fail to address systemic biases or adapt to complex, non-linear relationships in data. This project seeks to develop a machine learning pipeline that predicts loan approvals while addressing fairness concerns to ensure equitable access to credit across all demographic groups.

### Objectives

The goal of this project is to analyze and predict loan approvals while assessing financial risks associated with borrowers. This involves creating a classification model that predicts whether a loan will be approved (binary classification). Key objectives include:

- Clean and preprocess financial and demographic data.
- Engineer meaningful features for better predictive performance.
- Train and evaluate machine learning models.
- Interpret the results to support decision-making in financial risk management.

### Dataset

The dataset contains 20,000 records, including demographic and financial information such as age, income, credit history, and debt levels. It focuses on predicting serious delinquency (90+ days overdue).

### Solution Approach

#### Data Cleaning:
- Imputed missing values for MonthlyIncome and NumberOfDependents using median imputation.
- Removed outliers in Age outside the range of 18–100.
- Standardized features to ensure uniform scaling.

#### Exploratory Data Analysis (EDA):
- Visualized correlations using heatmaps and histograms to identify key predictors like RevolvingUtilizationOfUnsecuredLines and DebtRatio.
- Highlighted class imbalances in target variable distribution.

#### Feature Engineering:
- Created DebtToIncomeRatio (monthly debt payments divided by income) and NetWorth (assets minus liabilities) to capture financial stability.

#### Model Building:
- Trained multiple models (Logistic Regression, Random Forest, Gradient Boosting) to predict loan approvals.
- Introduced adversarial debiasing and fairness constraints to mitigate bias.

#### Evaluation:
- Used traditional metrics like accuracy (92.33%), precision, recall, and F1-score.
- Measured fairness using demographic parity and equalized odds to ensure ethical decision-making.

### Results

#### Performance:
- Accuracy: 92.33%, Precision (0): 93%, Precision (1): 91%, F1-score (1): 84%.
- Random Forest outperformed other models, achieving robust results while maintaining fairness.

#### Fairness Insights:
- Fairness constraints successfully reduced disparate impact between demographic groups, promoting equitable access to loans.

#### Key Visuals:
- ROC-AUC curves showed strong discrimination between risk classes.
- Bar charts compared fairness metrics across models.

### Key Insights

- High precision for approved loans (1), making the model suitable for reducing false positives in financial risk assessment.
- High recall for non-approved loans (0), ensuring fewer risky approvals.
- The DebtToIncomeRatio and NetWorth were significant features influencing loan approval predictions.

### Challenges

- Balancing high accuracy with fairness metrics required iterative testing and model adjustments.
- Addressing class imbalance involved careful resampling and weighting strategies.

### Source

https://www.kaggle.com/c/GiveMeSomeCredit
