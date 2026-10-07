# Credit Default Prediction Using Machine Learning (Python)

## Project Overview
This project focuses on predicting credit card default risk using a real-world dataset from a Taiwanese bank. The objective was to identify the demographic, behavioral, and credit-related factors most strongly associated with default and to develop predictive models that support better credit risk management.

## Project Structure

The analysis is organized into two main notebooks:

- **[Exploratory Data Analysis](notebooks/01_credit_default_eda.ipynb)** — Data quality checks, descriptive statistics, class imbalance analysis, demographic analysis, and exploratory visualizations.
- **[Predictive Modeling](notebooks/02_credit_default_modeling.ipynb)** — Statistical analysis, feature preparation, Logistic Regression and Random Forest modeling, model evaluation, and feature importance analysis.

## Tools & Technologies

**Programming & Data Analysis**
- Python
- Pandas
- NumPy

**Data Visualization**
- Matplotlib
- Seaborn

**Machine Learning**
- Scikit-learn
- Logistic Regression
- Random Forest

**Statistical Analysis**
- Independent t-tests
- Chi-square tests
- Descriptive statistics

**Model Evaluation**
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

## Dataset

The project uses the **Default of Credit Card Clients** dataset from the UCI Machine Learning Repository. The dataset contains **30,000 credit card clients** and information about their demographic characteristics, credit limits, repayment history, bill statements, and previous payments.

The main feature groups include:

- **Demographics:** Sex, education, marital status, and age
- **Credit Information:** Credit limit (`LIMIT_BAL`)
- **Repayment History:** Payment status variables (`PAY_0` to `PAY_6`)
- **Bill Statements:** Monthly bill amounts (`BILL_AMT1` to `BILL_AMT6`)
- **Previous Payments:** Monthly payment amounts (`PAY_AMT1` to `PAY_AMT6`)
- **Target Variable:** Whether the client defaulted on the following month's payment

The target variable is imbalanced:

- **Non-default:** 23,364 clients (77.88%)
- **Default:** 6,636 clients (22.12%)

This class imbalance was considered during model development and evaluation, particularly when comparing accuracy, precision, recall, F1-score, and ROC-AUC.

## Project Objectives
- Identify the key factors influencing credit card default risk
- Compare the predictive value of demographic variables versus payment behavior
- Build and evaluate machine learning models for default classification
- Translate predictive results into actionable business recommendations

## Methodology
The project workflow included:

1. Data collection and preprocessing
2. Exploratory data analysis
3. SQL-based exploratory queries
4. Statistical hypothesis testing using t-tests and chi-square tests
5. Data visualization in Python and Tableau
6. Model building with Logistic Regression and Random Forest
7. Model evaluation using classification metrics

## Statistical Testing
The project used:

- **t-tests** for continuous variables such as credit limit, bill amounts, and payment amounts
- **chi-square tests** for categorical variables such as education, marriage, and gender

Results showed that:
- Higher credit limits were associated with lower default risk
- Late payment indicators (PAY_0–PAY_6) had a very strong relationship with default
- Demographic variables were statistically significant, but less predictive than behavioral variables

## Models Built

### Logistic Regression
Used for interpretability and binary default classification.  
The model was trained using a 70/30 train-test split with feature scaling and class balancing.

### Random Forest
Used as a comparison model to capture nonlinear relationships and feature interactions.

## Model Evaluation
The report shows that:

- Logistic Regression with all features achieved **Accuracy = 0.73** and **ROC-AUC = 0.74**
- Random Forest achieved **Accuracy = 0.81** and **ROC-AUC = 0.76**
- Logistic Regression was selected for deployment because it had better recall for identifying risky customers, which better matched the business objective of minimizing missed defaults

## Key Insights
- Recent payment behavior was the strongest predictor of default
- Demographic variables alone performed poorly in prediction
- Behavioral and credit-related features provided the most predictive power
- Logistic Regression offered a good balance of interpretability and risk detection

## Business Impact
This project demonstrates how machine learning can support financial institutions by:

- Identifying high-risk customers earlier
- Improving credit risk monitoring
- Supporting data-driven lending decisions
- Reducing potential losses from default

## Contribution
This project was completed as part of a group assignment. My contributions included:

- Sourcing and proposing the dataset
- Developing the introduction, research questions, hypotheses, and methodology section
- Contributing to Python-based preprocessing, statistical testing, and model building
- Assisting with Logistic Regression and Random Forest implementation
- Supporting report writing and refinement
