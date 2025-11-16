# Predictive Analytics for Urban Air Quality: A Data-Driven Study of Dhaka

This repository contains the R code and analysis for a comprehensive data science project aimed at forecasting the Air Quality Index (AQI) in Dhaka. The primary goal is to transform a large-scale environmental dataset into a reliable forecasting tool capable of accurately predicting hazardous pollution events before they occur.

### 🎯 Project Goal

The core business problem is the critical information gap that forces public health and environmental agencies in Dhaka to be *reactive* rather than *proactive*. This project addresses that gap by developing a predictive framework to serve as a functional early warning system, enabling data-informed public health interventions and environmental governance.

### 📊 Key Findings

* **Chronic Unhealthy Air:** The mean AQI over the 25-year period was 173.9, a value firmly in the "Unhealthy" category.
* **Particulate Matter is the Driver:** Particulate matter (PM₂.₅ and PM₁₀) is the definitive driver of poor air quality, showing an exceptionally strong positive correlation with AQI (+0.97 for PM₂.₅).
* **Proven Seasonal Pattern:** Air quality is significantly worse in the dry winter months (December-February) and best during the monsoon season. This was statistically validated using ANOVA (p < 0.001).
* **High Predictive Accuracy:** The Random Forest regression model successfully explained over 91% (R² = 0.91) of the variance in AQI on unseen test data.
* **Reliable Forecasting:** An ARIMA time-series model successfully captured the seasonal rhythm of pollution and can reliably forecast future AQI trends.

### 🛠️ Methodology & Tools

This project followed a comprehensive data science workflow:

1.  **Data Preprocessing:** Parsing datetime features, capping outliers, and creating a binary target variable (`Hazardous`) for classification.
2.  **Exploratory Data Analysis (EDA):** Correlation analysis, descriptive statistics, and ANOVA testing to validate seasonal patterns.
3.  **Predictive Modelling (Regression):** Built Multiple Linear Regression (MLR) and Random Forest models to predict the continuous AQI value.
4.  **Time Series Forecasting:** Implemented an ARIMA model to forecast future daily AQI based on historical patterns.
5.  **Classification Modelling:** Trained Random Forest and XGBoost models to predict the likelihood of a "Hazardous" air quality event (AQI > 150).

* **Language:** **R**
* **Key Packages:** `tidyverse`, `forecast`, `randomForest`, `xgboost`, `caret`, `lubridate`

### 📁 Repository Structure

This diagram shows how the project files are organized:
/Dhaka-Air-Quality-Analysis
│
├── .gitignore
├── README.md
│
├── /code
│   ├── 01_data_preprocessing.R
│   ├── 02_eda_and_viz.R
│   ├── 03_regression_modeling.R
│   ├── 04_time_series_forecasting.R
│   └── 05_classification_modeling.R
│
└── /visuals
    ├── correlation_matrix.png
    ├── seasonal_boxplot.png
    └── arima_forecast_plot.png
    
### 🚀 Future Development

The models in this project serve as a strong foundation for a real-world application. Future steps include:

* **Operationalize Alert System:** Develop the high-performing classification model into a public-facing mobile app or SMS alert system.
* **Incorporate Real-Time Data:** Enhance accuracy by integrating live traffic data, satellite imagery, and land-use information.
* **Explore Deep Learning:** Investigate Long Short-Term Memory (LSTM) networks to potentially improve time-series forecasting accuracy.

### 🔗 Data Source

* **Name:** Dhaka Air Quality Dataset (2000–2025)
* **Source:** Kaggle
* **Author:** Mahmudul Hasan Akhand
