# Beyond the Credit Score: Evaluating Machine Learning Approaches to Loan Approval Prediction and the Role of Demographic Determinants in Consumer Lending

## Overview
Loan approval decisions in consumer lending extend far beyond credit scores alone. This project investigates the demographic and financial determinants of loan approval outcomes, comparing multiple machine learning algorithms to identify the most accurate and interpretable model for credit risk assessment.

## Research Aim
To evaluate machine learning approaches for loan approval prediction and examine the role of demographic determinants — including education, gender, and property location — in consumer lending decisions.

## Research Objectives
- Explore key demographic and financial factors influencing loan approval outcomes
- Handle real-world missing data through appropriate imputation techniques
- Build and compare multiple ML models for loan approval prediction
- Assess whether model complexity yields superior performance in credit scoring

## Research Questions
- What demographic and financial factors most strongly predict loan approval?
- Which machine learning algorithm most accurately predicts loan outcomes?
- Does model complexity always yield superior performance in credit scoring?

## Dataset
- Source: Loan Prediction Problem Dataset (Kaggle)
- 614 real loan applications with 13 features
- 68.7% approval rate — moderate class imbalance addressed using SMOTE
- Features include credit history, education, income, property area and loan amount

## Data Cleaning
Real-world dataset containing missing values across multiple columns including Credit History (50 missing), Self Employed (32 missing) and LoanAmount (22 missing). Missing categorical values imputed using mode and numerical values using median — a standard industry approach for credit data.

## Key Findings from Exploratory Analysis
- Credit history is the strongest predictor of loan approval — applicants with a positive credit history achieve an ~80% approval rate versus under 10% for those with adverse credit history
- Educational attainment positively correlates with approval — graduate applicants achieve a 70% approval rate versus 60% for non-graduates, suggesting lenders associate higher education with greater repayment capacity
- Semiurban properties yield the highest approval rate at ~75%, reflecting more stable collateral valuations compared to rural areas

## Models Compared

| Model | Accuracy | ROC-AUC |
|-------|----------|---------|
| Logistic Regression | 84% | 0.78 |
| Random Forest | 80% | 0.75 |
| Gradient Boosting | 79% | 0.73 |

## Conclusion
Logistic Regression outperforms both ensemble methods with the highest accuracy of 84% and ROC-AUC of 0.78 — demonstrating that model complexity does not always yield superior results, particularly on smaller datasets. Furthermore, in regulated financial services environments, Logistic Regression offers greater interpretability, enabling credit committees and regulators to understand and audit lending decisions — a critical compliance requirement in consumer lending.

## Tools & Libraries
Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, Matplotlib, Seaborn

## Author
**Lateefat Tobun** — MSc Applied AI & Data Analytics (Distinction), University of Bradford
