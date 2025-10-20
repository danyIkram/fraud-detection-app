# Fraud Detection Prediction App

An interactive **Fraud Detection System** built with **Streamlit** that predicts whether a financial transaction is fraudulent using a **Logistic Regression** model trained on a dataset of 6.3M transactions.

Dataset source: [Kaggle](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)

---

## Features

- Transaction type (`TRANSFER`, `CASH_OUT`, `PAYMENT`, `CASH_IN`, `DEBIT`)
- Transaction amount
- Sender balances (`oldbalanceOrg`, `newbalanceOrig`)
- Receiver balances (`oldbalanceDest`, `newbalanceDest`)
- Feature engineering: balance differences to detect suspicious activity
---

## Usage

Run the Streamlit app:

streamlit run fraud_detection.py


Enter transaction details: Transaction Type, Amount, Old/New Balance for Sender and Receiver. Click Predict to see if the transaction is likely fraudulent.

---

## Model

Algorithm: Logistic Regression

Class imbalance handled: class_weight="balanced"

Pipeline: Scaling numeric features + One-Hot encoding categorical features

Works best on TRANSFER and CASH_OUT transactions, which contain most frauds.

---

## Notes

Due to class imbalance, some high-risk transactions might still be predicted as non-fraudulent

Future improvements: use Random Forest, XGBoost, or anomaly detection for better fraud capture
