# 🚨📊 Fraudulent Claim Detection Case Study

## 🌟 Overview
Global Insure, an insurance company processing thousands of claims annually, faces significant financial losses due to fraudulent claims. The current manual fraud detection process is inefficient and often detects fraud too late. This project aims to enhance fraud detection by leveraging historical claim data and customer profiles to build a predictive model that classifies insurance claims as either fraudulent or legitimate. By identifying patterns and key indicators of fraud early in the approva...

## 🎯 Goal
The primary goal is to develop a data-driven solution that:
- 📈 Analyze historical claim data to detect patterns indicative of fraudulent claims.
- 🔑 Identify the most predictive features of fraudulent behavior.
- ⚡ Predict the likelihood of fraud for incoming claims based on past data.
- 🛠️ Provide actionable insights to improve the fraud detection process.

## ❓ Project Objectives
- 🕵️‍♂️ Pattern Detection: Analyze historical claim data to detect fraud-indicating patterns.
- 🌟 Feature Importance: Identify features that most strongly predict fraud.
- 📅 Fraud Prediction: Predict the probability of fraud for new claims.
- 💡 Process Improvement: Generate insights to optimize the claims review process.

## 🛠️ Methodology
We followed the CRISP-DM methodology:
- ✅ Business Understanding: Focused on recall for effective fraud detection.
- 🧹 Data Preparation: Cleaned and structured data for analysis.
- 🧼 Data Cleaning: Addressed missing values and corrected data types.
- ✂️ Data Splitting: Divided data into training and validation sets.
- 📊 EDA: Identified feature distributions and potential fraud signals.
- 🛠️ Feature Engineering: Derived new variables to improve prediction accuracy.
- 🤖 Model Building: Built Logistic Regression and Random Forest models.
- 🔍 Feature Selection: Used RFECV and Feature Importance metrics.
- ⚙️ Model Fine-Tuning: Optimized thresholds and hyperparameters with GridSearchCV.
- 📏 Model Evaluation: Measured using Accuracy, Recall, F1-Score.

## 🧪 Techniques Used
- 🔢 Data Preprocessing: One-Hot Encoding, Standard Scaling
- 🧠 Model Building: Logistic Regression, Random Forest
- 🎛️ Optimization: Cutoff tuning, GridSearchCV
- 📈 Evaluation: Accuracy, Confusion Matrix, Recall

## 🏆 Results

| Model              | Accuracy (Train) | Recall (Train) | Accuracy (Validation) | Recall (Validation) |
|-------------------|------------------|----------------|------------------------|----------------------|
| Logistic Regression | 86.6%            | 87.3%          | 84%                    | 90.5%                |
| Random Forest       | 90.4%            | 93.3%          | 77.7%                  | 75.7%                |

✅ Logistic Regression was selected as the best model due to its superior recall on validation data.

## 🌟 Significant Features

- `insured_hobbies_chess`: +4.2153 – strong fraud signal
- `insured_hobbies_cross-fit`: +3.5445 – strong fraud signal
- `insured_hobbies_dancing`: -22.7954 – low fraud risk
- `incident_severity_Minor Damage`: -3.4093 – low fraud risk
- `incident_severity_Total Loss`: -3.2046 – low fraud risk

### Regression Equation:

## 💡 Key Insights
- ⏳ Newer customers are more likely to commit fraud.
- 👶 Younger customers (under 30) have a higher fraud rate.
- 💸 Lower policy deductibles are linked with more fraud.
- 🎲🏋️‍♂️💃 Hobbies like chess & CrossFit → more fraud; dancing → less fraud.
- 🚗 Minor damage and total loss claims are less associated with fraud.

📈 **ROC Curve AUC**: 0.88 → Indicates strong model performance.

## 📋 Recommendations
- 🚩 Scrutinize claims with chess or CrossFit hobbies.
- ⚡ Fast-track minor damage and dancing-related claims.
- 🎯 Focus fraud detection on mid-severity claims (not total loss or minor).
