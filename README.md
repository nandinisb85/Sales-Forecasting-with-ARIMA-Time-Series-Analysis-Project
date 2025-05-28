# Sales-Forecasting-with-ARIMA-Time-Series-Analysis-Project

📌 Objective:
To analyze and forecast weekly sales for a retail store using time series methods, specifically ARIMA modeling, in Python.

🧾 Dataset:
Walmart dataset with features like Store, Date, Weekly_Sales, etc.

Filtered data for Store 1 to focus on a single time series.

🔧 Tools & Technologies:
Python Libraries: pandas, matplotlib, seaborn, statsmodels

Environment: Google Colab (Jupyter notebook environment)

📊 Key Steps:
Data Preprocessing

Parsed dates and sorted data.

Filtered for Store 1.

Aggregated weekly sales into monthly data for trend smoothing.

Exploratory Data Analysis (EDA)

Visualized sales trends over time.

Observed seasonal dips and spikes, suggesting potential for seasonal modeling.

Stationarity Check

Used ADF (Augmented Dickey-Fuller) Test to confirm the need for differencing.

Sales data was non-stationary, so differencing was applied to stabilize variance.

Model Identification

ACF and PACF plots used to estimate AR and MA components.

Determined suitable ARIMA parameters (p=1, d=1, q=1).

Model Fitting

Trained an ARIMA(1,1,1) model using statsmodels.

Checked model summary: MA(1) term significant, AR(1) less so.

Reasonable AIC/BIC values indicated a decent fit.

Residual Diagnostics

Residual plots showed no strong patterns.

Q-Q plot and histogram indicated approximate normality.

Ljung-Box test returned high p-values — confirming white-noise residuals.

📈 Results:
The ARIMA model captured the trend reasonably well.

The residuals showed minimal autocorrelation, supporting model adequacy.

This project demonstrates practical skills in:

Cleaning and preparing time series data

Model diagnostics and validation

Forecasting with ARIMA in a structured pipeline
