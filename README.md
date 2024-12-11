# Diagnosing Breast Cancer
This repository contains my attempt to apply a classification model to data from the WiDS Datathon 2024 Challenge.
https://www.kaggle.com/competitions/widsdatathon2024-challenge1/overview

## Overview
The goal, as described by the Kaggle challenge, is to use data taken from Health Verity on patients who are diagnosed with Metastatic Triple Negative Breast Cancer in the U.S. to predict whether the patient will be diagnosed within 90 days of screening. Delays in diagnosis and thus treatment can negatively impact the survivability of the disease. This project will analyze what factors contribute to significant gap between screening and diagnosis

## Summary of Work Done!

### Data
The training dataset contains 12,906 entries and the test dataset contains 5,791 entries, both in the form of csv files. They have 83 and 82 columns, respectively, with 12/13 of those being categorical/non-numerical.

### Pre-processing
I chose to ommit the variables 'breast_cancer_diagnosis_code', 'breast_cancer_diagnosis_desc', 'metastatic_cancer_diagnosis_code', 'metastatic_first_novel_treatment', and 'metastatic_first_novel_treatment_type'

### Data Visualization
The issue with this specific dataset is that there is very little correalation between our target variable and the other features. 

<img width="605" alt="Screenshot 2024-12-11 at 11 17 59 AM" src="https://github.com/user-attachments/assets/95bab021-cfac-4eee-b6fc-e43894234498" />

### Training
Naive Bayes: 58%

Logistic Regression: 63%

XGBoost: 59% Accuracy
### Performance Comparison
Logistic Regression had the highest accuracy score.
### Conclusions
