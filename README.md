# Climate-Change-Forecasting-Model

## Goal:

To develop a robust climate change forecasting model using SARIMAX to predict temperature fluctuations, aiming to improve forecast accuracy by minimizing prediction errors.


## Approach:

**Data Preparation and Initial Analysis:**
1. Extracted temperature data for Rio de Janeiro from the global dataset, focusing on monthly averages from 1900 to 2012.
2. Performed exploratory analysis using line plots and pivot tables to visualize both yearly and monthly variations.
3. Observed seasonality, with warmer months between November and February and cooler months between July and September.
   
**Trend Analysis:**
1. Calculated the yearly average temperatures and applied a 10-year moving average to smooth the trend.
2. Found an increasing trend in temperature, with the average temperature rising by approximately 4.25% over 100 years.
   
**Stationarity Check:**
1. Used the Augmented Dickey-Fuller (ADF) test to confirm that the series was stationary after seasonal differencing.
2. Plotted ACF and PACF, indicating a seasonal ARIMA model with AR(3) and seasonal SMA(1) components was appropriate.
   
**Modeling:**
1. Split the data into training (first ~100 years), validation (last 5 years), and test sets (last year).
2. Fitted a SARIMA(3,0,0)(0,1,1,12) model and made predictions using walk-forward validation.
3. Achieved an RMSE of 0.7874 for the SARIMA model, improving the baseline forecast (previous month's temperature) by over 40%.
