# 🛒 Walmart Sales Forecasting

📊 **Predictive Analytics | Time Series Forecasting | Machine Learning**

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab)](https://colab.research.google.com/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn)](https://scikit-learn.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-Time%20Series-4051B5)](https://www.statsmodels.org/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?logo=github)](https://github.com/)

A predictive analytics project for analyzing historical Walmart weekly sales and forecasting future sales using statistical time-series models and machine learning techniques.

---

## 📌 Project Overview

This project analyzes historical Walmart sales data to understand sales trends, seasonal patterns, weekly fluctuations, and relationships between sales and other available variables.

Multiple predictive approaches were implemented and evaluated:

- **ARIMA**
- **SARIMA**
- **Random Forest**

The models were evaluated using:

- **MAE — Mean Absolute Error**
- **RMSE — Root Mean Squared Error**
- **R² Score**

The primary forecasting target was **overall weekly Walmart sales**, obtained by aggregating sales across stores.

The final model comparison showed that **SARIMA** provided the best overall forecasting performance among the evaluated models.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze historical Walmart weekly sales.
- Perform data preprocessing and feature engineering.
- Explore trends and seasonal patterns.
- Analyze sales behavior across stores and time periods.
- Identify important patterns in historical sales.
- Build machine learning and time-series forecasting models.
- Compare model performance using standard evaluation metrics.
- Select the best-performing forecasting model.
- Forecast future weekly Walmart sales.
- Generate useful business insights from the forecasting results.

---

## 📊 Dataset

The project uses historical Walmart weekly sales data containing the following variables:

| Feature | Description |
|---|---|
| `Store` | Walmart store identifier |
| `Date` | Week/date of the recorded sales |
| `Weekly_Sales` | Weekly sales for each store |
| `Holiday_Flag` | Indicates whether the week contains a holiday |
| `Temperature` | Temperature during the week |
| `Fuel_Price` | Fuel price during the week |
| `CPI` | Consumer Price Index |
| `Unemployment` | Unemployment rate |

The dataset contains records from multiple Walmart stores across several years.

> **Dataset Source:** Walmart Sales Forecasting dataset obtained from Kaggle.

---

## 🛠️ Technologies Used

### Programming Language
- Python

### Data Analysis
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Machine Learning
- Scikit-learn

### Time-Series Forecasting
- Statsmodels

### Development Environment
- Google Colab

### Version Control
- GitHub

---

## 🔄 Project Workflow

```text
Historical Walmart Data
          ↓
Data Understanding
          ↓
Data Preprocessing
          ↓
Feature Engineering
          ↓
Exploratory Data Analysis
          ↓
Machine Learning Models
          ↓
Time-Series Models
          ↓
Model Validation
          ↓
Model Comparison
          ↓
Best Model Selection
          ↓
Future Sales Forecasting
          ↓
Business Insights
          ↓
Conclusion
```

---

## 🧹 Data Preprocessing

The dataset was prepared for analysis through the following steps:

- Inspected dataset structure and dimensions.
- Checked data types.
- Checked for missing values.
- Converted the `Date` column into datetime format.
- Sorted records chronologically.
- Created time-based features:
  - Year
  - Month
  - Week
- Aggregated store-level weekly sales to obtain overall Walmart weekly sales for time-series forecasting.

The dataset contained **6,435 records and 8 original variables**, with no missing values detected during preprocessing.

---

## 📈 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the behavior of Walmart sales over time.

The analysis included:

### Overall Sales Trend
Examined how total Walmart weekly sales changed over the historical period.

### Store-Wise Sales
Compared sales performance across different Walmart stores.

### Monthly Analysis
Analyzed changes in sales across different months.

### Yearly Analysis
Compared sales behavior across different years.

### Correlation Analysis
Examined relationships between weekly sales and numerical variables such as:

- Temperature
- Fuel Price
- CPI
- Unemployment

### Holiday Analysis
Compared sales behavior between holiday and non-holiday periods.

### Seasonal Analysis
Identified recurring patterns and fluctuations in weekly sales.

---

## 🤖 Models Implemented

### 1. Linear Regression

Linear Regression was initially used as a simple machine-learning baseline for predicting weekly sales using engineered features.

The model provided a baseline for comparison with the more advanced Random Forest approach.

---

### 2. Random Forest

Random Forest Regression was implemented as the primary machine-learning approach.

Features used included:

- Store
- Holiday Flag
- Temperature
- Fuel Price
- CPI
- Unemployment
- Year
- Month
- Week

The model was evaluated at the store-level and also aggregated to obtain overall weekly sales predictions.

The store-level Random Forest evaluation achieved an R² score of approximately **0.7246**.

However, for the final comparison with ARIMA and SARIMA, the **overall weekly sales evaluation** was used to maintain a consistent forecasting target.

---

### 3. ARIMA

ARIMA was implemented as a baseline time-series forecasting model.

The selected configuration was:

```text
ARIMA(1,1,1)
```

ARIMA models the temporal structure of the sales series but does not explicitly include a seasonal component.

---

### 4. SARIMA

SARIMA was implemented to capture both non-seasonal and seasonal patterns in Walmart's weekly sales.

The selected configuration was:

```text
SARIMA(1,1,1)(1,1,1,52)
```

A seasonal period of **52 weeks** was used to represent yearly seasonality in the weekly sales data.

---

## 📏 Model Evaluation Metrics

The models were evaluated using three primary metrics.

### MAE — Mean Absolute Error

MAE measures the average absolute difference between actual and predicted values.

**Lower MAE indicates better performance.**

### RMSE — Root Mean Squared Error

RMSE measures prediction error while assigning greater importance to larger errors.

**Lower RMSE indicates better performance.**

### R² Score

R² measures how well the model explains the variation in the target variable.

**Higher R² indicates better performance.**

---

## 🏆 Final Model Comparison

The following results are based on the **overall weekly Walmart sales validation**:

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| ARIMA(1,1,1) | 1,377,592.95 | 1,887,425.72 | -0.6048 |
| **SARIMA(1,1,1)(1,1,1,52)** | **760,840.46** | **890,763.33** | **0.6426** |
| Random Forest | 1,760,779.93 | 2,263,701.72 | 0.1362 |

### 🥇 Best Model: SARIMA

Based on the final overall-sales validation:

**SARIMA(1,1,1)(1,1,1,52)** achieved the best performance.

### SARIMA Performance

- **MAE:** 760,840.46
- **RMSE:** 890,763.33
- **R² Score:** 0.6426

SARIMA achieved the lowest MAE and RMSE and the highest R² Score among the three models in the final comparison.

This indicates that incorporating the yearly seasonal pattern was useful for forecasting Walmart's weekly sales.

---

## 🔮 Future Sales Forecast

The selected SARIMA model was used to forecast Walmart's weekly sales for the next **12 weeks**.

### Forecast Summary

| Metric | Value |
|---|---:|
| Average Forecasted Weekly Sales | ~53.12 million |
| Highest Forecasted Weekly Sales | ~77.94 million |
| Lowest Forecasted Weekly Sales | ~42.87 million |
| Forecast Horizon | 12 weeks |

The forecast shows noticeable variations across the predicted weeks, reflecting the seasonal patterns captured by the SARIMA model.

> **Note:** Forecast values are analytical estimates based on historical sales patterns and should not be interpreted as guaranteed future sales.

---

## 📊 Forecast Visualization

The final notebook contains a visualization comparing:

- Historical overall Walmart weekly sales
- SARIMA predicted sales
- Start of the forecast period

This visualization helps understand how the forecast extends beyond the historical data.

---

## 💼 Business Insights

The analysis provides several potential business insights:

- Walmart weekly sales demonstrate noticeable seasonal fluctuations.
- Incorporating yearly seasonality improved forecasting performance.
- Forecasts can support inventory and demand planning.
- Expected sales peaks can help businesses prepare for periods of higher demand.
- Forecasted declines can assist with inventory and resource management.
- Historical sales patterns can support supply-chain planning.
- Forecast information can assist with sales and promotional planning.

---

## 📓 Google Colab Notebook

The complete implementation and analysis are available in Google Colab.

👉 **[Open Project in Google Colab](YOUR_COLAB_LINK)**

The notebook contains:

- Data preprocessing
- Exploratory data analysis
- Feature engineering
- Linear Regression
- Random Forest
- ARIMA
- SARIMA
- Model validation
- Model comparison
- Future sales forecasting
- Forecast visualization
- Business insights

> Replace `YOUR_COLAB_LINK` with the shareable Google Colab URL of the notebook.

---

## 📂 Repository Contents

```text
Walmart-Sales-Forecasting/
│
├── Predictive_Analytics_Using_Historical_Walmart_Data.ipynb
└── README.md
```

The dataset itself is not included in this repository. The notebook uses the Walmart dataset obtained from Kaggle.

---

## ▶️ How to Run the Project

### Option 1 — Google Colab

1. Open the Google Colab notebook.
2. Upload the Walmart dataset when prompted.
3. Run the notebook cells sequentially.
4. Review the EDA visualizations and model results.
5. View the final SARIMA forecast.

### Option 2 — Jupyter Notebook

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

Then open:

```text
Predictive_Analytics_Using_Historical_Walmart_Data.ipynb
```

and execute the cells sequentially.

---

## ⚠️ Limitations

The project has several limitations:

- Forecast accuracy depends on the historical data available.
- Future external factors may affect actual Walmart sales.
- The SARIMA model primarily captures historical temporal and seasonal patterns.
- The forecast should be considered an analytical estimate rather than a guaranteed outcome.
- Additional external variables and more advanced validation strategies could potentially improve performance.

---

## 🚀 Future Improvements

Possible improvements include:

- Systematic hyperparameter tuning.
- Testing XGBoost and other advanced machine-learning models.
- Exploring additional time-series forecasting methods.
- Applying rolling-window or expanding-window validation.
- Incorporating additional external economic variables.
- Building an interactive dashboard using Streamlit or Power BI.
- Deploying the forecasting model as an API or web application.
- Automating periodic sales forecasting.

---

## 📝 Conclusion

This project demonstrates how predictive analytics, machine learning, and time-series forecasting can be applied to historical retail sales data.

Multiple approaches were implemented, including Linear Regression, Random Forest, ARIMA, and SARIMA.

For the final overall weekly sales forecasting comparison, **SARIMA(1,1,1)(1,1,1,52)** achieved the best performance with:

- **MAE:** 760,840.46
- **RMSE:** 890,763.33
- **R² Score:** 0.6426

The results highlight the importance of incorporating seasonal patterns when forecasting weekly retail sales.

The project demonstrates how forecasting techniques can support data-driven decisions related to demand planning, inventory management, resource allocation, and sales strategy.

---

## 👨‍💻 Author

**Shubham Sharma**

B.Tech Computer Science & Engineering

---

⭐ If you found this project useful, consider giving the repository a star!
