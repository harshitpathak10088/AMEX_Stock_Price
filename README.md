# 📈 AMEX Stock Price Forecasting using ARIMA

This project forecasts **American Express (AMEX/AXP)** stock prices using **time-series modeling techniques**.  
The analysis applies the **Box–Jenkins ARIMA methodology** and benchmarks against **Holt–Winters exponential smoothing** to evaluate predictive performance under different regimes.  

---

## 🚀 Objectives

- Analyze historical AMEX stock price data.  
- Test for **stationarity** and transform the series as required.  
- Build, optimize, and evaluate **ARIMA models**.  
- Compare ARIMA against **Holt–Winters exponential smoothing**.  
- Forecast AMEX stock prices for the next 12 months.  

---

## 🗂 Repository Structure

AMEX_Stock_Price/
├── AXP_Historical_Data.csv # Historical daily stock prices
├── CodeNotebook.py # Python script for EDA, ARIMA modeling, forecasting
├── Project_Report.pdf # Detailed report (methodology, results, insights)
└── README.md # Project overview and instructions


---

## 🔑 Key Contributions

- **Optimized ARIMA(4,1,1)** on log-differenced AMEX series; minimized RMSE via Box–Jenkins model, PACF tuning, and residual correction.  
- **Validated I(1) series** using **ADF and KPSS tests**; applied differencing and rolling variance bands to detect drift, non-stationarity, and volatility clustering.  
- **Benchmarked Holt–Winters vs ARIMA** under non-Gaussian regimes; tuned smoothing factors and analyzed residual tails via **KDE kurtosis**.  

---

## 📊 Methodology

1. **Exploratory Data Analysis (EDA):**  
   - Visualized price trends and volume.  
   - Calculated rolling means and standard deviations.  

2. **Stationarity Testing:**  
   - Augmented Dickey-Fuller (ADF) and KPSS tests.  
   - Applied differencing and log transformations.  

3. **Modeling:**  
   - Fitted ARIMA(p,d,q) models using Box–Jenkins approach.  
   - Tuned PACF/ACF lags for AR and MA order selection.  

4. **Forecasting & Validation:**  
   - Train-test split (2020–2022 train, 2023 test).  
   - Forecasted 12-month stock prices.  
   - Benchmarked ARIMA vs Holt–Winters.  

5. **Residual Diagnostics:**  
   - White noise checks.  
   - KDE plots of residuals to confirm near-Gaussian distribution.  

