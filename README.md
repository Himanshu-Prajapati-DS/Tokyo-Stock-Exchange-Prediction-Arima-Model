# 📈 Stock Price Forecasting using ARIMA Time Series Model

## Overview

This project demonstrates the implementation of the **Autoregressive Integrated Moving Average (ARIMA)** model for forecasting next-day stock opening prices using historical stock market data.

The project follows a complete time series forecasting workflow, including data preprocessing, stationarity testing, parameter optimization using Auto ARIMA, model training, prediction, and performance evaluation.

---

## Business Problem

Financial markets generate large volumes of sequential data, making accurate stock price forecasting a challenging task.

The objective of this project is to develop an ARIMA-based forecasting model capable of predicting the **next day's opening stock price** from historical market data.

---

## Dataset

**Source:** JPX Tokyo Stock Exchange Prediction Dataset (Kaggle)
https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data
The dataset contains historical stock market data from the Tokyo Stock Exchange between **2017 and 2022**.

### Features

- Date
- Securities Code
- Open Price
- High Price
- Low Price
- Close Price
- Volume
- Adjustment Factor
- Expected Dividend
- Supervision Flag

For this project, one company (**Kotobuki Spirits Co., Ltd.**) was selected for detailed time series analysis.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- pmdarima
- Scikit-learn
- Jupyter Notebook

---

## Project Workflow

```

Historical Stock Data
│
├── Data Cleaning
│
├── Exploratory Data Analysis
│
├── Feature Selection
│
├── Stationarity Test (ADF Test)
│
├── Auto ARIMA
│
├── ARIMA Model
│
├── Forecasting
│
├── Performance Evaluation
│
└── Visualization

```

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed missing values
- Selected relevant features
- Converted date columns into datetime format
- Filtered data for a single company
- Split dataset into training and testing sets (70:30)

---

## Exploratory Data Analysis

EDA included:

- Descriptive Statistics
- Correlation Heatmap
- Time Series Visualization
- KDE Distribution Plot
- Boxplots
- Volume Analysis

---

## Stationarity Testing

Since ARIMA requires stationary data, the **Augmented Dickey-Fuller (ADF) Test** was performed.

The analysis showed that the original series was non-stationary and required differencing before model training.

---

## Auto ARIMA

Auto ARIMA was used to automatically determine the optimal model parameters.

Selected parameters:

```

ARIMA(0,1,1)

```

The optimal model was selected using:

- AIC
- BIC
- Log-Likelihood

---

## Model Training

The ARIMA model was trained using the optimized parameters obtained from Auto ARIMA.

The model learned historical trends and generated one-step-ahead forecasts for the stock opening price.

---

## Model Evaluation

Performance was evaluated using:

- RMSE (Root Mean Square Error)
- MAPE (Mean Absolute Percentage Error)

| Metric | Value |
|---------|-------|
| RMSE | 887.39 |
| MAPE | 11.07% |

---

## Results

The ARIMA model successfully captured the overall trend of the stock price and produced reliable short-term forecasts.

Key observations:

- Good performance for short-term forecasting
- Forecasts closely followed the historical trend
- Suitable for linear time series data
- Performance decreases during highly volatile market periods

---

## Visualizations

The project includes:

- Historical Stock Price
- Forecast Plot
- Auto ARIMA Diagnostics
- Residual Analysis
- ACF Plot
- Prediction vs Actual Values

---

## Repository Structure

```

stock-price-arima/
│
├── data/
│   └── stock_data.csv
│
├── notebooks/
│   └── ARIMA_Model.ipynb
│
├── images/
│   ├── forecast.png
│   ├── diagnostics.png
│   ├── adf_test.png
│   ├── residuals.png
│   └── prediction.png
│
├── requirements.txt
├── README.md
└── LICENSE

```

---

## Key Learnings

- Time Series Analysis
- Stationarity Testing
- ARIMA Modeling
- Auto ARIMA Optimization
- Forecast Evaluation
- Time Series Visualization
- Feature Selection
- Model Diagnostics

---

## Future Improvements

Potential enhancements include:

- Seasonal ARIMA (SARIMA)
- Facebook Prophet
- LSTM-based forecasting
- Hybrid ARIMA-LSTM models
- Incorporating news sentiment and macroeconomic indicators
- Hyperparameter optimization

---

## References

- Box, G. E. P., Jenkins, G. M., Reinsel, G. C.
- Statsmodels Documentation
- pmdarima Documentation
- JPX Tokyo Stock Exchange Dataset

---

## Author

**Himanshukumar Prajapati**

- GitHub: https://github.com/Himanshu-Prajapati-DS
- LinkedIn: www.linkedin.com/in/himanshu-prajapati-7514a849

---

⭐ If you found this project useful, please consider giving it a star!
