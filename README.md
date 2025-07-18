Credit Card Fraud Detection
This project focuses on detecting fraudulent transactions using machine learning techniques. The dataset is highly imbalanced, which presents a real-world challenge for classification models.

📁 Dataset
Source: Kaggle - Credit Card Fraud Detection

Rows: 284,807 transactions

Features: 30 (including anonymized principal components V1 to V28, Time, and Amount)

Target: Class (0 → Legitimate, 1 → Fraud)

🧹 Data Preprocessing
Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique)

Applied StandardScaler on Amount and Time

No missing values in the dataset

Split into train and test sets (80/20)

📊 Exploratory Data Analysis
Only 0.17% of transactions are fraudulent

Most fraudulent transactions have smaller amounts

Time of transaction had no clear pattern for fraud detection

Features V1–V28 are PCA components and cannot be interpreted directly

🤖 Models Trained
Model	Accuracy	Precision	Recall	F1 Score	ROC-AUC
Logistic Regression					
Random Forest					
XGBoost					

✅ Final Model Selection
Selected Model: XGBoost

Justification: Best trade-off between precision and recall (since false negatives are critical in fraud detection), highest ROC-AUC.
📈 Evaluation Metrics
Confusion Matrix

Precision, Recall, F1 Score

ROC-AUC Curve

PR Curve (useful for imbalanced datasets)

🧠 Key Learnings
Class imbalance handling is critical — recall is often prioritized in fraud detection.

Ensemble methods like Random Forest and XGBoost work well out of the box.

Evaluation should focus on Recall and AUC, not just Accuracy.
