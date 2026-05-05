# 🔒 Online Payments Fraud Detection using ML

A Machine Learning-based system to detect and prevent fraudulent financial transactions in real-time using advanced classification models.

---

## 📌 Overview

The **Online Payment Fraud Detection System** is an end-to-end machine learning pipeline designed to identify fraudulent transactions with high accuracy and speed. It simulates real-world financial behavior using synthetic data and applies multiple ML models to detect anomalies.

This system demonstrates a complete data science workflow:

- Data generation  
- Feature engineering  
- Handling class imbalance  
- Model training & evaluation  
- Production-ready inference API  

The goal is to build a scalable and reliable fraud detection mechanism suitable for financial applications such as banking, fintech apps, and e-commerce platforms.

---

## 🚀 Key Features

### ⚙️ Machine Learning Pipeline
- Synthetic dataset with 50,000 transactions  
- Realistic fraud rate simulation (2.5%)  
- Advanced feature engineering (behavioral + transactional patterns)  
- SMOTE for handling imbalanced datasets  

---

### 🤖 Models Used
- Logistic Regression (baseline)  
- Random Forest (best performing)  
- XGBoost (boosted ensemble model)  

---

### 📊 Performance
- ROC-AUC: 1.0000 (all models)  
- Precision & Recall: Near perfect classification  
- Optimized threshold-based classification system  

---

### ⚡ Real-Time Detection
- Sub-10ms inference time  
- Risk scoring system (LOW / MEDIUM / HIGH)  
- Production-ready `FraudDetector` API class  

---

## 🏗️ System Architecture

The system follows a structured ML pipeline:

### 1. Data Generation
- Simulates realistic financial transactions  
- Includes fraud patterns (time, amount, location-based behavior)  

### 2. Feature Engineering
- Log transformation of amount  
- Risk scoring features  
- Temporal behavior analysis  

### 3. Data Preprocessing
- Encoding categorical variables  
- Scaling numerical features  
- Handling missing values  

### 4. Model Training
- Multiple algorithms trained in parallel  
- Hyperparameter tuning  
- Cross-validation evaluation  

### 5. Evaluation
- Confusion matrix analysis  
- ROC-AUC comparison  
- Feature importance ranking  

### 6. Deployment
- Serialized model using Joblib  
- Real-time prediction API  

---

## 🚨 Fraud Detection Logic

The system detects fraud using behavioral and transactional patterns:

### Key Fraud Indicators
1. Transactions during unusual hours (late night activity)  
2. Extremely high transaction amounts  
3. Very new accounts with high-value transactions  
4. International transactions  
5. Device switching patterns  
6. Risky merchant categories (online/travel)  

---

## 📊 Dataset Description

| Feature | Description |
|----------|-------------|
| amount | Transaction value |
| hour_of_day | Time of transaction |
| merchant_category | Type of merchant |
| payment_method | Credit / Debit / Wallet |
| account_age_days | Age of account |
| num_prev_txns | Previous transactions |
| device_type | Mobile / Desktop |
| is_international | Cross-border flag |
| is_fraud | Target label |

- Total records: 50,000  
- Fraud cases: ~2.5%  
- Balanced using SMOTE  

---

## 🤖 Model Performance

| Model | Accuracy | ROC-AUC | Notes |
|------|----------|---------|------|
| Logistic Regression | 99%+ | 1.0000 | Fast baseline |
| Random Forest | 100% | 1.0000 | Best overall |
| XGBoost | 100% | 1.0000 | Highly optimized |

---

## 🏆 Selected Model: Random Forest

Chosen due to:
- Perfect classification accuracy  
- Strong feature interpretability  
- Stable performance on imbalanced data  
- Fast inference speed  

---

## ⚡ FraudDetector API

A production-ready module for real-time fraud prediction.

Supports:
- Transaction scoring  
- Risk classification  
- Probability estimation  
- Threshold-based decision making  

---

## 📁 Project Structure

```text
fraud-detection-system/
│
├── data/               # Raw & processed datasets
├── notebooks/          # EDA and training notebooks
├── src/                # Core ML pipeline code
├── models/             # Saved trained models
├── reports/            # Visualizations & analysis
├── docs/               # Documentation
├── README.md
