# Fraud-Detection-Project

## Overview
This project focuses on detecting fraudulent transactions using machine learning. We use RandomForestClassifier and XGBoostClassifier to build models and improve their performance through data preprocessing, class balancing, and hyperparameter tuning.

## Dataset

- The dataset contains the following features:
- step: Time step of the transaction
- type: Type of transaction\
- amount: Transaction amount
- oldbalanceOrg: Initial balance of the origin account
- newbalanceOrig: New balance of the origin account
- oldbalanceDest: Initial balance of the destination account
- newbalanceDest: New balance of the destination account
- isFlaggedFraud: Fraud label (0 = no, 1 = yes)

## Data Preprocessing

- Categorical features are encoded properly.
- Missing values are handled if any exist.
- Class imbalance is handled using SMOTE to oversample fraud transactions.
- Scaling and PCA are used where needed.

## Models
- RandomForestClassifier
- XGBoostClassifier (with enable_categorical=True for categorical features)
