# Forecasting Australian CPI Using Time Series Models

## Executive Summary

This project investigates the forecasting of Australia's Consumer Price Index (CPI) using quarterly data from 1990 Q1 to 2019 Q4. The objective was to develop and compare multiple forecasting approaches and identify the most suitable model for predicting CPI values for 2020–2021.

The analysis began with exploratory data analysis and stationarity testing. Results from the Augmented Dickey-Fuller (ADF) test indicated that the CPI series was non-stationary and exhibited a strong long-term upward trend. First-order differencing was therefore applied before fitting time series models.

Four forecasting techniques were evaluated:

* Linear Regression
* Polynomial Regression
* Simple Exponential Smoothing (SES)
* ARIMA

Model performance was assessed using RMSE, MAE, and MAPE. Among the baseline models, ARIMA(1,1,1) achieved the best forecasting accuracy, outperforming both regression-based approaches and SES.

To further improve model performance, residual diagnostics and automated model selection were conducted using Auto-ARIMA. The optimisation process identified ARIMA(2,1,2) as the preferred specification, reducing forecast errors substantially.

### Final Model Performance

| Model                  | RMSE  | MAE   | MAPE (%) |
| ---------------------- | ----- | ----- | -------- |
| ARIMA(1,1,1)           | 1.154 | 0.933 | 0.827    |
| Optimised ARIMA(2,1,2) | 0.970 | 0.703 | 0.635    |

The optimised ARIMA model achieved approximately:

* 16% reduction in RMSE
* 25% reduction in MAE
* 23% reduction in MAPE

compared with the original ARIMA model.

The final model was used to forecast Australian CPI for 2020–2021, producing stable and economically realistic projections that continued the long-term inflation trend observed in historical data.

## Key Skills Demonstrated

* Time Series Analysis
* Forecasting and Predictive Modelling
* ARIMA Modelling
* Auto-ARIMA Optimisation
* Stationarity Testing (ADF)
* Residual Diagnostics
* Model Evaluation (RMSE, MAE, MAPE)
* Python (Pandas, NumPy, Statsmodels, Scikit-learn, Matplotlib)
* Data Visualisation

## Technologies Used

Python, Pandas, NumPy, Statsmodels, Scikit-learn, Matplotlib, Seaborn, pmdarima
