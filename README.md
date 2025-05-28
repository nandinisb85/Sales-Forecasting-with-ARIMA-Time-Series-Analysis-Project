# Sales-Forecasting-with-ARIMA-Time-Series-Analysis-Project

## 📌 Objective
Forecast weekly sales for a Walmart retail store using ARIMA time series modeling techniques in Python.

---

## 📁 Dataset
- Source: Walmart Sales Data
- Focus: Store 1 (`Weekly_Sales` over `Date`)
- Frequency: Weekly data aggregated to monthly for modeling

---

## 🛠 Tools & Technologies
- Python Libraries: `pandas`, `matplotlib`, `seaborn`, `statsmodels`
- Environment: Google Colab / Jupyter Notebook

---

## 📊 Workflow

### 1. Data Preparation
- Converted `Date` column to datetime format
- Filtered dataset for Store 1
- Aggregated weekly sales to monthly totals for smoother trends

### 2. Exploratory Data Analysis (EDA)
- Plotted sales trend over time
- Identified seasonality and general trend patterns

### 3. Stationarity Check
- Applied Augmented Dickey-Fuller (ADF) test
- Sales series was non-stationary → differenced once (`d=1`)

### 4. Model Identification
- Used ACF and PACF plots to estimate:
  - Autoregressive terms (p)
  - Moving Average terms (q)
- Selected ARIMA(1,1,1) based on visual and statistical cues

### 5. Model Training
- Fit ARIMA model using `statsmodels.tsa.ARIMA`
- Evaluated model with AIC/BIC metrics
- AR term: weakly significant, MA term: strongly significant

### 6. Residual Diagnostics
- Checked residuals for randomness (white noise)
- Plotted residual histogram, Q-Q plot, and ACF
- Ljung-Box test: High p-values → residuals are uncorrelated

---

## 📈 Results
- Forecasting model captured overall trend well
- Minimal autocorrelation in residuals supports model quality
- ARIMA(1,1,1) chosen as the final model for prediction

---

## ✅ Key Learnings
- Importance of making time series stationary before modeling
- Visual tools (ACF, PACF) are powerful for model design
- ARIMA models require careful tuning and diagnostics

---

## 🧠 Future Improvements
- Try SARIMA to capture seasonality explicitly
- Incorporate external regressors (e.g., holidays, promotions)
- Use cross-validation for better model robustness

