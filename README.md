# 🏦 Bank Customer Churn Prediction – Logistic Regression

## 1️⃣ Project Overview

This project builds a binary classification model to predict whether a bank customer will churn (leave the bank) using a **Logistic Regression** model.  
The dataset contains **600 customers** with information about their age, balance, credit score, tenure, card/active status, and churn label (0 = stayed, 1 = churned).

### 🎯 Main Goals
- 📊 Explore the data and generate summary statistics and visualizations  
- 🤖 Train and evaluate a logistic regression model for churn prediction  
- 📁 Export a CSV file containing both actual and predicted churn values  

---

## 2️⃣ Dataset

Columns used (after loading `bank_churn.csv`):

- 🆔 `ID` – unique customer identifier  
- 🟢 `active_member` – 1 if active, 0 otherwise  
- 🎂 `age` – customer age (20–78)  
- 💰 `balance` – account balance  
- 💳 `credit_card` – 1 if the customer has a credit card, 0 otherwise  
- 📈 `credit_score` – credit score (≈350–850)  
- 📅 `tenure` – number of years with the bank (0–10)  
- 🔁 `churn` – target label (0 = not churned, 1 = churned)

### 📌 Basic Properties
- 🧮 Shape: **(600, 8)**  
- 🔢 All columns are numeric  
- ⚖️ Perfectly balanced classes: **300 non-churn (0)** and **300 churn (1)**  

---

## 3️⃣ Exploratory Data Analysis – Key Insights

### 📈 3.1 Summary Statistics
From `df.describe()`:
- 📊 **Average Age:** ~41.4 years  
- 💰 **Average Balance:** ~84,874 (many customers have 0 balance)  
- 📉 **Credit Score:** avg ~649, most values between 590–707  
- 📅 **Tenure:** ranges 0–10 years, median ≈ 5  

---

## 📉 3.2 Visual Insights (Graphs)

- 🧮 **Churn Distribution**  
  Balanced 50% churn / 50% non-churn

- 📦 **Credit Score Boxplot**  
  Highlights a low-score outlier (~350)

- 📊 **Churn Count by Age**  
  Shows churn patterns across age groups

- 🟢 **Churn vs Active Member Status**  
  Relationship between activity and churn

- 💳 **Churn vs Credit Card Ownership**  
  Compare churn between those with/without a credit card

- 💰 **Churn vs Balance Threshold**  
  Boolean split: `balance < 107688.905`

---

## 4️⃣ Model Performance – Accuracy Score

After training the Logistic Regression model, two accuracy scores were computed:

### ✅ Training Accuracy
0.7375


### ✅ Test Accuracy
0.7833


### 📝 Interpretation
- 📌 The model performs **better on unseen test data** → good generalization  
- 📌 Test accuracy of **78.3%** indicates the model predicts churn reasonably well  
- ⚠️ No signs of overfitting, since training accuracy is slightly lower  

---


