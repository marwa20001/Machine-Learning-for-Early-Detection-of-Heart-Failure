Predictive Analytics and Machine Learning for Early Detection of Heart Failure: A Business Intelligence Framework Based on Real-World Clinical Data
Heart Failure Prediction Using Machine Learning

 Introduction

Heart failure (HF) is a major public health issue globally, with over 64 million people affected. Despite clinical guidelines and treatments, many diagnoses come late, increasing death rates and healthcare costs. This project applies predictive analytics and machine learning to early heart failure detection, using a dataset from Kaggle.

Objectives

Use ML models to predict early heart failure

Identify top clinical predictors (e.g., ejection fraction, serum creatinine)

Evaluate performance using accuracy, recall, AUC, etc.

Dataset

Source:   from Kaggle          https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data

Records: 299 patients

Features: 13 (e.g., age, ejection fraction, creatinine, diabetes, smoking, etc.)

Target: DEATH_EVENT (0 = survived, 1 = died)

 Data Preprocessing

No missing values

All variables were numerical

Used MinMaxScaler to normalize data

Train-test split: 80% training / 20% testing

📊 Exploratory Data Analysis (EDA)

Found inverse correlation between ejection fraction & DEATH_EVENT

High serum creatinine levels associated with mortality

Used scatter plots and histograms to visualize distributions

Imbalanced classes but manageable

Machine Learning Applications

1. Unsupervised Learning - KMeans Clustering

Applied to group patients by risk

Chose k=3 using Elbow Method

Used PCA to reduce dimensions for visualization

Resulted in 3 distinct health-risk groups:

Cluster 0: High-risk (low EF, high creatinine)

Cluster 1: Moderate-risk

Cluster 2: Low-risk, stable patients

2. Supervised Learning - Random Forest Classifier

Goal: Predict DEATH_EVENT

Achieved 83% accuracy, AUC = 0.87

Important features: ejection fraction, serum creatinine

Used: accuracy, precision, recall, F1-score, confusion matrix

 Results Summary

Metric

Value

Accuracy

83%

AUC

0.87

Key Features

EF, serum creatinine

Clusters differed significantly in risk profile and suggested actionable insights for medical decisions.

 Business Impact

Helps doctors triage patients early

Can be embedded into EHRs

Prevents ICU admissions, reduces costs

Assists in preventive care for low-risk groups

 Limitations

Small dataset (n=299), from a single location

KMeans assumptions may not always hold

Further validation needed
