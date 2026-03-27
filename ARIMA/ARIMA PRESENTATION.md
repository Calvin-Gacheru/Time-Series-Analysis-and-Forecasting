# GROUP FOUR: ARIMA MODELS
## Introduction
ARIMA (AutoRegressive Integrated Moving Average) is a powerful time series forecasting method that combines autoregressive (AR) and moving average (MA) components, along with differencing to achieve stationarity. It is widely used for forecasting non-seasonal time series data. SARIMA (Seasonal ARIMA) extends ARIMA to handle seasonality in the data, making it suitable for datasets with strong seasonal patterns.

## AR Models
AR models predict future values based on a linear combination of past values. The order of the AR model (p) indicates how many past values are used in the prediction. 

$$y_t = c + \phi_1 y_{t-1} + \phi_2 y_{t-2} + \ldots + \phi_p y_{t-p} + \epsilon_t$$

## MA Models
MA models predict future values based on a linear combination of past forecast errors. The order of the MA model (q) indicates how many past forecast errors are used in the prediction.
$$y_t = c + \epsilon_t + \theta_1 \epsilon_{t-1} + \theta_2 \epsilon_{t-2} + \ldots + \theta_q \epsilon_{t-q}$$

## ARMA Models
ARMA models combine both AR and MA components. The order of the ARMA model is denoted as (p, q), where p is the order of the AR part and q is the order of the MA part.
$$y_t = c + \phi_1 y_{t-1} + \ldots + \phi_p y_{t-p} + \epsilon_t + \theta_1 \epsilon_{t-1} + \ldots + \theta_q \epsilon_{t-q}$$

## ARIMA Models
ARIMA models include an additional differencing step to achieve stationarity. The order of the ARIMA model is denoted as (p, d, q), where d is the order of differencing. This indicates how many times the data needs to be differenced to achieve stationarity.

$$y_t' = c + \phi_1 y_{t-1}' + \ldots + \phi_p y_{t-p}' + \epsilon_t + \theta_1 \epsilon_{t-1} + \ldots + \theta_q \epsilon_{t-q}$$

Where $y_t' = \nabla^d y_t$ is the differenced series.
 
This is simply predicting the change in the data, not the actual data itself. The model learns to predict how much the data will change from one time step to the next, rather than predicting the absolute value of the data at each time step. This is a crucial distinction that allows ARIMA models to handle non-stationary data effectively.