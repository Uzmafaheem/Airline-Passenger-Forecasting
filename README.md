# Airline Passenger Time Series Forecasting 📈

## Forecasting monthly airline passenger numbers using ARIMA, SARIMA, and smoothing methods.

This repository provides a complete, step-by-step guide to time series analysis, covering data transformation, stationarity testing, model building, and forecasting. It demonstrates how simple smoothing methods compare with advanced statistical models like ARIMA and SARIMA.

## Project Objective

The goal of this project is to forecast monthly airline passenger demand using statistical time series methods, exploring different modeling approaches, and selecting the model that best captures both trend and seasonality.

## 📂 About the Dataset

The dataset used in this project is the Airline Passengers Dataset, a classic time series dataset widely used for forecasting practice.

Dataset Details

- Description: Monthly totals of international airline passengers (in units) from January 1949 to December 1960.

- Size: 144 observations (12 years × 12 months)

- Columns:

    - Month – Date of observation (YYYY-MM format)

    - Passengers – Number of passengers

## Core Concepts Covered

- Time Series Fundamentals: Understanding trend, seasonality, and residuals.

- Stationarity: Testing using Augmented Dickey-Fuller (ADF) test.

- Data Transformation: Log transformation, first differencing, and seasonal differencing.

- Model Identification: Using ACF and PACF plots to determine ARIMA parameters.

- Modeling Approaches:

   - Moving Average

   - Exponential Smoothing (Simple & Double)

   - ARIMA

   - SARIMA

- Forecasting & Evaluation: Comparing model performance and visualization.

## Stationarity Testing

- Original Series: Non-stationary (p-value ≈ 0.991)

- Log + First Differencing: Still non-stationary (p-value ≈ 0.071)

- After Seasonal Differencing (Lag = 12): Stationary (p-value ≈ 0.0002)

Conclusion: Seasonal differencing is necessary to achieve stationarity due to strong annual patterns.

## Model Identification

- PACF Plot: Cuts off after lag 1 → suggests p = 1

- ACF Plot: Cuts off after lag 1 → suggests q = 1

Initial Model Choice: ARIMA(1,1,1)

## Comparison of Methods

| Method                           | Performance                                                                                                                             |
| -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Moving Average**               | Smooths short-term noise and highlights trend, but misses seasonal fluctuations. Poor for forecasting seasonal data.                    |
| **Double Exponential Smoothing** | Follows trend better than moving average, but still fails to capture seasonality.                                                       |
| **ARIMA**                        | Captures overall trend after differencing but misses seasonal patterns.                                                                 |
| **SARIMA**                       | Effectively captures both trend and seasonality. Forecast aligns closely with actual data. Best performance for airline passenger data. |


## Visual Summary:

- Moving Average: lagging and misses seasonality

- Double Exponential: better trend-following, still misses seasonal peaks

- ARIMA: models trend well, but ignores seasonal peaks

- SARIMA: accurately captures trend and seasonal fluctuations

## Business Impact

- Accurately forecasting airline passenger demand has significant operational and strategic value:

- Revenue Optimization: Adjust pricing, promotions, and capacity planning.

- Resource Planning: Schedule flights, crew, and maintenance efficiently.

- Inventory Management: Allocate seats and services optimally.

- Strategic Decision-Making: Supports long-term planning for route expansion, fleet management, and marketing campaigns.

Using SARIMA enables actionable insights that simpler models cannot provide, especially for seasonal data.

## Solution Overview

- Data Transformation: Log transformation + first differencing + seasonal differencing to stabilize variance and remove trend/seasonality.

- Stationarity Testing: ADF test confirms series stationarity.

- Modeling Approaches: Moving Average, Exponential Smoothing, ARIMA, SARIMA.

- Parameter Selection: ACF & PACF used to identify ARIMA/SARIMA orders.

- Forecasting: SARIMA effectively captures trend and seasonality, outperforming other models.

## Key Takeaways

- Airline passenger data is strongly seasonal, requiring careful transformations before modeling.

- SARIMA is the most effective model, accurately forecasting both trend and seasonality.

- Simple smoothing or standard ARIMA models are insufficient for seasonal datasets.

- The workflow demonstrates a reproducible approach to time series forecasting applicable to other industries.

## References

Box & Jenkins (1976) – Time Series Analysis: Forecasting and Control

Statsmodels SARIMAX Documentation

## 🛠 How to Run the Project

- Download

- Open on google colab or Jupyter Notebook

- Run all

## 👤 Author
Faheemunnisa Syeda Machine Learning & Applied Math Specialist

- 📧 syedafaheem7@gmail.com
- 🔗 GitHub: [https://github.com/syedafaheem7/]
- 🔗 linkedln: [https://www.linkedin.com/in/faheem-unnisa-s-6270888b/]
