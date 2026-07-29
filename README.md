# Time Series Forecasting of Electricity Demand

A time series forecasting project that predicts monthly electricity demand in the ISO New England region using Seasonal ARIMA (SARIMA). Developed as part of MA585: Time Series and Forecasting at Boston University.


## Project Overview

This project applies the Box-Jenkins methodology to forecast monthly Non-Peak Time Frame (Non-PTF) electricity demand in the ISO New England Control Area. The objective was to develop an accurate forecasting model for electricity demand and compare its performance with a classical exponential smoothing approach.


## Dataset

- **Source:** ISO New England Public Data Portal
- **Region:** ISO New England (Connecticut, Maine, Massachusetts, New Hampshire, Rhode Island, and Vermont)
- **Time Period:** January 2017 – December 2024
- **Frequency:** Monthly
- **Target Variable:** Non-Peak Time Frame (Non-PTF) Demand (GWh) 


## Models

- **SARIMA(0,1,1) × (0,1,1)₁₂**
- **Holt-Winters Exponential Smoothing (Additive)**


## Results

<p align="center">
  <img src="figures/SARIMA_train.png" width="850">
</p>

| Model | MAE | RMSE | MAPE |
|--------|----:|-----:|------:|
| SARIMA | 306.37 | 381.98 | 3.11% |
| Holt-Winters | 395.63 | 485.64 | 4.01% |

The SARIMA model consistently outperformed the Holt-Winters model across all evaluation metrics, producing more accurate forecasts while better capturing seasonal demand fluctuations. 


## Future Improvements

- Incorporate exogenous variables such as temperature and economic indicators using SARIMAX.
- Explore advanced forecasting approaches such as Prophet and LSTM models.
- Evaluate model performance over longer forecasting horizons. 
