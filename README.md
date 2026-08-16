# Walmart Sales Forecasting

📊 **Predictive Analytics | Time Series Forecasting | Machine Learning**

A predictive analytics project for analyzing historical Walmart weekly sales and forecasting future sales using statistical time-series models and machine learning.

---

## 📌 Project Overview

This project analyzes historical Walmart sales data to identify sales patterns, trends, seasonal behavior, and factors influencing weekly sales.

Multiple forecasting approaches were implemented and compared:

- ARIMA
- SARIMA
- Random Forest

The models were evaluated using **MAE, RMSE, and R² Score** to determine the most effective forecasting approach.

---

## 🎯 Objectives

- Analyze historical Walmart weekly sales.
- Perform data preprocessing and feature preparation.
- Identify trends and seasonal patterns.
- Build multiple predictive models.
- Compare model performance using evaluation metrics.
- Forecast future Walmart sales.
- Generate useful business insights from the forecasts.

---

## 📊 Dataset

The project uses historical Walmart weekly sales data containing information such as:

- Date
- Store
- Weekly Sales
- Holiday Flag
- Temperature
- Fuel Price
- CPI
- Unemployment

The data covers multiple Walmart stores over several years.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Statsmodels
- Google Colab
- GitHub

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
Model Development
          ↓
Model Evaluation
          ↓
Model Comparison
          ↓
Future Sales Forecasting
          ↓
Business Insights
```

---

## 📈 Exploratory Data Analysis

The historical sales data was analyzed to identify:

- Overall sales trends
- Weekly sales fluctuations
- Seasonal patterns
- Major sales peaks and declines
- Changes in sales behavior over time

---

## 🤖 Models Implemented

### ARIMA

Used as a baseline time-series forecasting model.

### SARIMA

Used to capture both trend and seasonal patterns in weekly sales.

Configuration:

`SARIMA(1,1,1)(1,1,1,52)`

The seasonal period of 52 weeks was used to capture yearly seasonality.

### Random Forest

A machine-learning regression model using features such as Store, Holiday Flag, Temperature, Fuel Price, CPI, Unemployment, Year, Month, and Week.

---

## 🏆 Model Comparison

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| ARIMA(1,1,1) | 1,377,592.95 | 1,887,425.72 | -0.6048 |
| SARIMA(1,1,1)(1,1,1,52) | 760,840.46 | 890,763.33 | 0.6426 |
| Random Forest | 1,760,779.93 | 2,263,701.72 | 0.1362 |

### 🥇 Best Model

**SARIMA(1,1,1)(1,1,1,52)** achieved the best overall performance.

- MAE: **760,840.46**
- RMSE: **890,763.33**
- R² Score: **0.6426**

The results indicate that incorporating seasonal patterns significantly improved forecasting performance.

---

## 🔮 Forecast Results

The selected SARIMA model was used to forecast future weekly Walmart sales.

The forecast was visualized alongside historical sales to compare expected future sales behavior with historical patterns.

---

## 💼 Business Insights

The analysis provides several useful insights:

- Walmart sales exhibit noticeable seasonal fluctuations.
- Seasonal forecasting performs better than the tested non-seasonal ARIMA model.
- Forecasts can support inventory and demand planning.
- Expected sales peaks can help businesses prepare for higher demand.
- Forecasted declines can assist in resource and inventory management.

---

## 📝 Conclusion

This project demonstrates how predictive analytics and time-series forecasting can be used to analyze and forecast Walmart weekly sales.

Among the evaluated models, SARIMA achieved the best performance with an R² Score of **0.6426** and the lowest MAE and RMSE.

The results highlight the importance of incorporating seasonal patterns when forecasting weekly retail sales.

---

## 🚀 Future Improvements

- Hyperparameter tuning
- Testing XGBoost and other ML models
- Testing additional forecasting methods
- Rolling-window time-series validation
- Interactive dashboard using Streamlit or Power BI
- Deployment of the forecasting model as an API

---

## 👨‍💻 Author

**Shubham Sharma**

B.Tech Computer Science & Engineering
