Fraud Detection with Machine Learning

Project Overview

This project aims to build a fraud detection model using transactional data of over 6 million records. The dataset includes anonymized financial transactions with a small fraction of fraudulent cases. The main objective is to identify fraudulent transactions using machine learning, advanced feature engineering, and handling extreme class imbalance.

Dataset

The dataset consists of 6.3M+ transactions with the following features:
Transaction type (PAYMENT, TRANSFER, CASH_OUT, etc.)
Amount transferred
Origin and destination balances before and after transaction
Fraud label (isFraud)
Flagged fraud label (isFlaggedFraud)
Note: The dataset was preloaded from [source if public] or provided for educational purposes.
Key Steps

1️⃣ Data Cleaning & Exploration
Checked for missing values and duplicates
Explored transaction type distributions
Analyzed fraud distribution across transaction types

2️⃣ Feature Engineering
Created new features:
amount_class (binning amount values)
log_amount (log-transformed amounts)
balance changes (origin & destination balance gaps)
full_transfer_ratio (amount / origin balance)
Encoded categorical variables using one-hot and ordinal encoding
Handled missing values for merchants vs customers

3️⃣ Modeling
Train-test split with stratification to preserve fraud ratio
Built an XGBoost classifier with hyperparameter tuning
Addressed class imbalance using scale_pos_weight

4️⃣ Evaluation

Achieved:
ROC AUC Score: 0.9997
F1 Score: 0.8745
Plotted confusion matrix, ROC curve, and feature importance
Model Performance

Metric	Score
ROC AUC	99.97%
F1 Score	87.45%
Accuracy	~100% (due to class imbalance)
Technologies Used

Python
Pandas
NumPy
Matplotlib / Seaborn
Scikit-learn
XGBoost
Plotly
Folder Structure

📦fraud-detection
 ┣ 📂data
 ┃ ┗ fraud.csv
 ┣ 📂notebooks
 ┃ ┗ fraud_detection_notebook.ipynb
 ┣ 📄 README.md
 ┗ 📄 requirements.txt
 
Acknowledgements

Dataset used purely for educational and personal project purp
