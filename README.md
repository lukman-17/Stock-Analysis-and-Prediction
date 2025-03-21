# Stock Analysis and Prediction

## Overview
This project focuses on analyzing stock market data by fetching live data from Yahoo Finance using the `yfinance` library. The analysis involves performing Exploratory Data Analysis (EDA) and using technical indicators such as the 10-day Exponential Moving Average (EMA), 20-day EMA, and 50-day EMA. Additionally, predictive modeling techniques including SARIMA, ARIMA, and LSTM are implemented to forecast stock prices, with LSTM showing the best performance.

## Data Collection
- The stock data is fetched in real-time using the `yfinance` library.
- It includes various features like Open, High, Low, Close, Volume, and Adjusted Close prices.
- The dataset is processed to ensure completeness before analysis.

## Exploratory Data Analysis (EDA)
EDA is performed to understand the underlying patterns in the stock market data:
- **Visualization of stock price trends** to analyze historical behavior.
- **Calculation of Exponential Moving Averages (EMAs):**
  - 10-day EMA
  - 20-day EMA
  - 50-day EMA
- **Identification of stock trends using EMA crossovers.**
- **Checking for seasonality and trends** in stock price movements.
- **Statistical summary of stock data** to evaluate the distribution of values.

## Predictive Analytics
Several time series forecasting models are implemented to predict stock prices:

### 1. **ARIMA (AutoRegressive Integrated Moving Average)**
- ARIMA is used for univariate time series forecasting.
- The model parameters (p, d, q) are selected based on ACF and PACF plots.
- The model is trained on historical stock prices and evaluated based on error metrics.

### 2. **SARIMA (Seasonal ARIMA)**
- SARIMA extends ARIMA by incorporating seasonal components.
- The seasonal parameters (P, D, Q, s) are fine-tuned to improve accuracy.
- The model is evaluated using Mean Squared Error (MSE) and Mean Absolute Error (MAE).

### 3. **LSTM (Long Short-Term Memory Networks)**
- LSTM, a type of Recurrent Neural Network (RNN), is used to capture long-term dependencies in stock price movements.
- The dataset is split into training and testing sets.
- Data is scaled using MinMaxScaler before feeding into the LSTM model.
- The model is trained using multiple layers to improve prediction accuracy.
- **LSTM outperforms ARIMA and SARIMA in terms of prediction accuracy.**

## Key Findings
- **EMA analysis** helps identify potential buy/sell signals based on trend reversals.
- **ARIMA and SARIMA models** work well for short-term predictions but struggle with long-term accuracy.
- **LSTM model significantly improves forecasting accuracy** by capturing complex patterns in stock price movements.

## Conclusion
This project successfully demonstrates how stock market data can be analyzed using technical indicators and how different time series forecasting models perform in predicting future stock prices. The LSTM model proves to be the most effective approach, providing more accurate forecasts compared to ARIMA and SARIMA models.

## Future Improvements
- Implementing other deep learning models like Transformer-based architectures for stock prediction.
- Incorporating additional features like sentiment analysis from financial news.
- Using ensemble techniques to combine the strengths of multiple models for better accuracy.

## Dependencies
To run this project, install the required dependencies:
```bash
pip install yfinance pandas numpy matplotlib seaborn statsmodels tensorflow keras
```

## Usage
Run the Jupyter Notebook to fetch stock data, perform EDA, and apply predictive models.
```bash
jupyter notebook Stock_Analysis.ipynb
```

## Author
- Lukman Qureshi
- https://github.com/lukman-17/

##Stock Price Fluctuations
  ![image](https://github.com/user-attachments/assets/318c9326-055e-42cc-b1ec-680fa5d6975b)

## Stock Price EMA 10 days, 20 days, 50 days
![image](https://github.com/user-attachments/assets/324e5e77-95e4-4b18-ac12-131158114aeb)

##LSTM Model Predictions on Test Data
![image](https://github.com/user-attachments/assets/6496dad6-bf90-42d7-98c8-00d53b854e09)




