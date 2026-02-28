# 🚕 Taxi Demand Time Series Forecast  
Hourly Order Prediction Using Time-Based Modeling

---

## 📖 Project Overview

This project forecasts hourly taxi demand based on historical airport order data. The objective is to predict the number of taxi orders for the next hour in order to support driver allocation during peak demand periods.

The final model must achieve an RMSE below 48 on the test set.

---

## 🎯 Business Objective

- Predict hourly taxi demand  
- Improve driver allocation during peak periods  
- Build a time-aware forecasting model  
- Achieve RMSE ≤ 48 on the test set  

---

## 🗂 Data

- Historical taxi order dataset  
- Target variable: **num_orders**  
- Data resampled to hourly intervals  

---

## 🛠️ Methodology

### 1️⃣ Data Preparation
- Datetime parsing and indexing  
- Hourly resampling  
- Creation of time-based features (lag features and rolling averages)  

### 2️⃣ Exploratory Analysis
- Trend analysis  
- Seasonality identification  
- Autocorrelation evaluation  

### 3️⃣ Model Training
Multiple regression models were evaluated with hyperparameter tuning, including:

- Linear Regression (baseline)
- Decision Tree Regressor
- Random Forest Regressor

The dataset was split chronologically, with the last 10% used as the test set.

---

## 📊 Evaluation Metric

- **RMSE (Root Mean Squared Error)**  

---

## 📊 Results

| Model | RMSE |
|--------|------|
| Linear Regression | ~54 |
| Decision Tree | ~50 |
| Random Forest | ~44 |

The Random Forest model achieved the best performance with an RMSE of approximately **44**, meeting the project requirement (RMSE ≤ 48).

---

## 📈 Key Findings

- Time-based features (lags and rolling statistics) significantly improved forecasting accuracy.  
- Tree-based models outperformed linear regression.  
- Random Forest provided the best balance between prediction accuracy and stability.  

---

## 🧰 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
