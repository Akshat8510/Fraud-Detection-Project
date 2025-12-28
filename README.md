# 🛡️ Online Transaction Fraud Detection

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![XGBoost](https://img.shields.io/badge/Algorithm-XGBoost-green.svg)

## 📌 Project Overview
This project identifies fraudulent activity in financial transactions using a dataset of 6.3M+ records. The core challenge is the extreme class imbalance (only 0.13% are fraud). I implemented a multi-iteration approach using **SMOTE** and **XGBoost** to reach near-optimal detection levels.

## 📊 Key Results
Through 5 iterations of data engineering and balancing, the models achieved the following performance:

| Iteration | Strategy | XGBoost AUC | Random Forest AUC |
| :--- | :--- | :--- | :--- |
| 1 | Baseline (Default Params) | 87% | 86% |
| 2 | Hyperparameter Tuning | 99.5% | 84.3% |
| 3 | SMOTE + Tuning | 99.4% | 98.7% |
| 4 | Undersampling + Tuning | 98.8% | 99.6% |
| 5 | **SMOTE + Subsampling** | **99.0%** | **92.1%** |

## 🛠️ Feature Importance
The analysis revealed that the most influential features for detecting fraud are:
1. `oldbalanceOrg` (Balance before transaction)
2. `newbalanceDest` (Recipient's new balance)
3. `amount` (Size of the transaction)

## 📂 Project Structure
```text
├── Fraud_detection.ipynb  # Main analysis and model training
├── requirements.txt       # Dependencies
├── .gitignore             # Excludes large data files
└── README.md              # Project documentation
```

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/Akshat8510/Fraud-Detection-Project.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook `Fraud_detection.ipynb`.
