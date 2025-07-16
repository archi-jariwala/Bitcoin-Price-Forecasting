# 📈 Bitcoin Price Forecasting Using Time Series & Deep Learning

This project explores and compares statistical and deep learning models for short-term forecasting of **Bitcoin closing prices** using high-frequency OHLCV (Open, High, Low, Close, Volume) data. By applying both classical time series methods and advanced neural networks, the project aims to capture the complex and volatile behavior of cryptocurrency markets.

---

## 🧠 Overview

With Bitcoin's extreme volatility and real-time trading nature, accurate short-term price prediction is challenging yet crucial for traders, analysts, and researchers. This project uses **minute-level Bitcoin data from 2012–2025**, resampled to hourly intervals, to build models that can predict the next hour’s closing price.

---

## 🔍 Key Features

### 📊 Exploratory Data Analysis (EDA)
- Identified missing data
- Resampled to hourly frequency
- Conducted correlation analysis between features

### ⚙️ Time Series Processing
- Performed ADF test for stationarity
- Applied first-order differencing
- Decomposed series into trend, seasonal, and residual components
- Generated ACF/PACF plots to guide model selection

### 📉 Statistical Forecasting Models
- Implemented **ARIMA**, **SARIMA**, and **SARIMAX** models
- Tuned model order using **AIC**
- Conducted residual diagnostics for model validity

### 🤖 Deep Learning Models
- Built and evaluated **RNN**, **LSTM**, and **GRU** models
- Developed a **multi-feature GRU** model using `Close`, `Open`, and `MA30` as inputs
- Applied **hyperparameter tuning**, **dropout**, and **early stopping** for performance optimization

---

## 🧪 Model Evaluation

Models were compared using the following metrics:
- **RMSE**: Root Mean Squared Error
- **MAE**: Mean Absolute Error
- **MAPE**: Mean Absolute Percentage Error
- **R²**: Coefficient of Determination

### ✅ Best Performing Model: Multi-Feature GRU
- **RMSE**: 188.5  
- **R²**: 0.9999  
- **MAPE**: 0.33%

---

## 🛠️ Tools & Technologies

- **Languages**: Python  
- **Libraries**:
  - NumPy, Pandas
  - Matplotlib, Seaborn
  - Statsmodels, Scikit-learn
  - TensorFlow, Keras

- **Models**:
  - ARIMA, SARIMA, SARIMAX
  - RNN, LSTM, GRU

---

## 📊 Results Summary

| Model             | RMSE   | MAE    | R² Score | MAPE   |
|------------------|--------|--------|----------|--------|
| ARIMA            | ~2500  | ~1650  | ~0.82    | ~6.8%  |
| SARIMA           | ~7500  | ~6600  | Very Low | High   |
| RNN              | 323.3  | 161.0  | 0.9998   | 0.36%  |
| LSTM             | 499.3  | 275.6  | 0.9997   | 0.66%  |
| GRU              | 427.3  | 349.7  | 0.9996   | 0.90%  |
| **Multi-Feature GRU** | **188.5** | **118.3** | **0.9999** | **0.33%** |

---

## 📌 Conclusion

- Classical models like **ARIMA** perform reasonably for trend-following behavior but fail under high volatility.
- Deep learning models, especially **GRU with engineered features**, drastically outperform traditional methods.
- **Feature selection** and **model tuning** are critical for improving forecasting performance, especially in noisy financial time series.

---

## 📁 Repository Structure

