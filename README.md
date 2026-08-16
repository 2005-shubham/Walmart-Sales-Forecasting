# Walmart Sales Forecasting

📊 **Predictive Analytics | Time Series Forecasting | Machine Learning**

A predictive analytics project for analyzing historical Walmart weekly sales and forecasting future sales using statistical time-series models and machine learning techniques.

---

## 📌 Project Overview

This project analyzes historical Walmart sales data to understand sales trends, seasonal patterns, weekly fluctuations, and relationships between sales and other available variables.

Multiple predictive approaches were implemented and evaluated:

- ARIMA
- SARIMA
- Random Forest

The models were evaluated using **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **R² Score** to determine the most effective approach for overall weekly sales forecasting.

---

## 🎯 Objectives

- Analyze historical Walmart weekly sales.
- Perform data preprocessing and feature engineering.
- Identify trends and seasonal patterns.
- Explore sales behavior across stores and time periods.
- Build machine learning and time-series forecasting models.
- Compare model performance using standard evaluation metrics.
- Forecast future weekly Walmart sales.
- Generate useful business insights from the forecasting results.

---

## 📊 Dataset

The project uses historical Walmart weekly sales data containing the following variables:

- **Store** – Walmart store identifier
- **Date** – Week/date of the recorded sales
- **Weekly_Sales** – Weekly sales for each store
- **Holiday_Flag** – Indicates whether the week contains a holiday
- **Temperature** – Temperature during the week
- **Fuel_Price** – Fuel price during the week
- **CPI** – Consumer Price Index
- **Unemployment** – Unemployment rate

The dataset contains records from multiple Walmart stores across several years.

> **Dataset Source:** Walmart Sales Forecasting dataset obtained from Kaggle.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Scikit-learn**
- **Statsmodels**
- **Google Colab**
- **GitHub**

---

## 🔄 Project Workflow

```text
Historical Walmart Data
          ↓
Data Preprocessing
          ↓
Exploratory Data Analysis
          ↓
Feature Engineering
          ↓
Machine Learning Models
          ↓
Time-Series Models
          ↓
Model Evaluation
          ↓
Model Comparison
          ↓
Best Model Selection
          ↓
Future Sales Forecasting
          ↓
Business Insights
