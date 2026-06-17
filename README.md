🏥 Patient Readmission Data Analysis System

A machine learning-based system to predict and analyze hospital readmission patterns using the Diabetes 130-US Hospitals dataset.

📌 Overview

Hospital readmission is a critical challenge in healthcare that affects patient outcomes and increases operational costs. This project presents a Patient Readmission Data Analysis System that leverages machine learning techniques to analyze diabetic patient records and predict the likelihood of hospital readmission within 30 days.
By identifying high-risk patients early, healthcare providers can take proactive measures to reduce unnecessary readmissions, improve patient care, and optimize hospital resources.

Problem Statement:

Hospital readmission of diabetic patients is a major healthcare challenge that leads to increased medical costs and poor patient outcomes. This project aims to analyze patient records and predict the likelihood of readmission within 30 days using machine learning techniques.

🎯 Objectives

Analyze the Diabetes 130-US Hospitals dataset to uncover readmission trends
Perform data preprocessing, feature engineering, and exploratory data analysis (EDA)
Build and evaluate machine learning models to predict patient readmission
Identify the most significant clinical and demographic factors influencing readmission
Provide actionable insights to support clinical decision-making

🛠️ Technologies Used

CategoryTools / LibrariesLanguagePython 3.xData ProcessingPandas, NumPyVisualizationMatplotlib, SeabornMachine LearningScikit-learnModel EvaluationScikit-learn Metrics, Confusion Matrix, ROC-AUCNotebook EnvironmentJupyter Notebook / Google ColabVersion ControlGit, GitHub

📂 Dataset Features


Dataset: Diabetes 130-US Hospitals for Years 1999–2008

Records: ~101,766 patient encounters

Features: 50 attributes

Key Features

FeatureDescriptionencounter_idUnique identifier for each hospital visitpatient_nbrUnique patient identifierracePatient's racegenderPatient's genderageAge group (in 10-year intervals)admission_type_idType of admission (emergency, urgent, elective, etc.)time_in_hospitalNumber of days spent in the hospitalnum_lab_proceduresNumber of lab tests performednum_proceduresNumber of non-lab procedures performednum_medicationsNumber of distinct medications administerednumber_outpatientNumber of outpatient visits in the prior yearnumber_emergencyNumber of emergency visits in the prior yearnumber_inpatientNumber of inpatient visits in the prior yeardiag_1 / diag_2 / diag_3Primary, secondary, and tertiary diagnosesnumber_diagnosesTotal number of diagnoses entered into the systemA1CresultHbA1c test resultinsulinInsulin dosage change indicatorchangeIndicator of change in diabetic medicationsdiabetesMedWhether diabetic medication was prescribedreadmittedTarget variable — <30 (readmitted within 30 days), >30, or NO

🤖 Machine Learning Models

The following models were trained and evaluated for predicting patient readmission:

ModelDescriptionLogistic RegressionBaseline linear classifierDecision TreeInterpretable tree-based modelRandom ForestEnsemble of decision trees for improved accuracyGradient BoostingBoosted ensemble for handling class imbalanceXGBoostOptimized gradient boosting with regularization

Model Pipeline

Data Cleaning & Null Handling
Label Encoding / One-Hot Encoding for categorical features
Feature Selection using Correlation & Feature Importance
Train-Test Split (80% / 20%)
Model Training & Hyperparameter Tuning
Evaluation using Accuracy, Precision, Recall, F1-Score, and ROC-AUC

🔄 Project Workflow

Data Collection
Data Preprocessing
Exploratory Data Analysis (EDA)
Feature Engineering
Model Training
Model Evaluation

Key Findings

Number of inpatient visits, time in hospital, and number of diagnoses are the strongest predictors of readmission
Patients with HbA1c test results recorded showed significantly lower readmission rates
Insulin administration changes correlated with higher readmission likelihood
Age group 60–80 had the highest readmission frequency

📊 Result Analysis

The bar chart above shows the Top 10 Factors Predicting Patient Readmission using the Random Forest model.
Key Observations

num_lab_procedures is the most influential factor (~0.31), indicating that patients with more lab tests have higher readmission risk
num_medications ranks second (~0.21), showing that complex medication regimens are strongly linked to readmission
time_in_hospital (~0.12) suggests longer stays correlate with higher readmission likelihood
num_procedures and number_diagnoses are moderate predictors, reflecting patient complexity
number_inpatient and number_outpatient prior visits also contribute to readmission prediction
race, gender, and number_emergency have relatively lower but still notable importance


<img width="1192" height="502" alt="Screenshot 2026-06-17 104755" src="https://github.com/user-attachments/assets/2e5d6193-5cd9-452f-900a-5d8cc10d3d54" />




✅ Conclusion

This project successfully demonstrates the application of machine learning to predict diabetic patient readmissions using real-world clinical data. The XGBoost model delivered the best performance, highlighting the value of ensemble methods for imbalanced healthcare datasets.

Key takeaways:

Early identification of high-risk patients can enable targeted interventions
HbA1c monitoring and medication management play a vital role in reducing readmissions
Integrating predictive models into clinical workflows can significantly improve patient outcomes and reduce hospital costs
Future enhancements may include:
Deep learning models (LSTM for temporal patient data)
Integration with Electronic Health Records (EHR) systems
Real-time readmission risk dashboards for clinicians


