# Diagnosing Breast Cancer
This repository contains my attempt to apply a classification model to data from the WiDS Datathon 2024 Challenge.
https://www.kaggle.com/competitions/widsdatathon2024-challenge1/overview

## Overview
The goal, as described by the Kaggle challenge, is to use data taken from Health Verity on patients who are diagnosed with Metastatic Triple Negative Breast Cancer in the U.S. to predict whether the patient will be diagnosed within 90 days of screening. Delays in diagnosis and thus treatment can negatively impact the survivability of the disease. This project will analyze what factors contribute to significant gap between screening and diagnosis. The best accuracy I got was 63% while the highest kaggle score I saw was around 80%.

## Summary

### Data

#### Train
12,906 rows, 83 columns

#### Test
5,791 rows, 82 columns

#### Target Variable
DiagPeriodL90D where 1 represents that the patient was dianosed within 90 days of screening and 0 represents that the patient was not diagnosed within 90 days of screening.

### Pre-processing
I chose to ommit the variables 'breast_cancer_diagnosis_code', 'breast_cancer_diagnosis_desc', 'metastatic_cancer_diagnosis_code', 'metastatic_first_novel_treatment', and 'metastatic_first_novel_treatment_type'

### Data Visualization
The issue with this specific dataset is that there is very little correalation between our target variable and the other features. 

<img width="896" alt="Screenshot 2024-12-13 at 3 30 39 PM" src="https://github.com/user-attachments/assets/fdb75f93-fbb4-4ece-b074-ebdc7398225e" />

<img width="896" alt="Screenshot 2024-12-13 at 3 30 39 PM" src="https://github.com/user-attachments/assets/1f763025-09be-463d-8291-6a7fca463691" />

<img width="919" alt="Screenshot 2024-12-13 at 3 30 11 PM" src="https://github.com/user-attachments/assets/c590a72c-05f2-4b26-901f-871f4f15d051" />

<img width="555" alt="Screenshot 2024-12-13 at 3 34 19 PM" src="https://github.com/user-attachments/assets/d000c6f8-acbe-4d74-b515-8c319672aef5" />

### Training
Naive Bayes: 58%

Logistic Regression: 63%

<img width="652" alt="Screenshot 2024-12-13 at 3 34 59 PM" src="https://github.com/user-attachments/assets/d747b177-3c6d-4057-b2fc-b3562fdbbecb" />

XGBoost: 59% Accuracy
### Performance Comparison
Logistic Regression had the highest accuracy score.
### Conclusions
