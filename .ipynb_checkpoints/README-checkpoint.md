# StockPredictor: A LSTM-Based Stock Price Prediction Model

## Overview
StockPredictor is a Python-based machine learning model designed to predict stock prices using historical data and technical indicators. It leverages Long Short-Term Memory (LSTM) networks to make accurate future stock price predictions. 

## Features
- Fetches historical stock data from Yahoo Finance
- Cleans and preprocesses stock data
- Computes key technical indicators:
  - Moving Averages (MA20, MA50)
  - Relative Strength Index (RSI)
  - Moving Average Convergence Divergence (MACD)
- Scales data for LSTM training
- Builds and trains LSTM models for each stock symbol
- Evaluates model performance using:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - R-squared Score (R2)
- Predicts future stock prices for the next 30 days
- Plots historical and predicted stock prices

## Dependencies
Ensure you have the following Python libraries installed:

```sh
pip install numpy pandas yfinance scikit-learn tensorflow matplotlib
```

## Usage
### 1. Initialize the StockPredictor
```python
from stock_predictor import StockPredictor

symbols = ['AAPL', 'GOOGL']  # List of stock symbols
start_date = '2022-01-01'
end_date = '2024-01-01'
predictor = StockPredictor(symbols, start_date, end_date)
```

### 2. Fetch Historical Data
```python
predictor.fetch_data()
```

### 3. Train the Model
```python
predictor.train_models(epochs=50, batch_size=32)
```

### 4. Make Predictions
```python
predictions = predictor.predict_next_days(days=30)
```

### 5. Plot Results
```python
predictor.plot_predictions(predictions)
```

## Model Evaluation Metrics
During training, the model outputs key evaluation metrics:
- **MSE (Mean Squared Error):** Measures average squared prediction error.
- **MAE (Mean Absolute Error):** Measures average absolute prediction error.
- **R2 Score:** Represents the goodness of fit (values close to 1 indicate strong model performance).

## License
This project is open-source and free to use for educational and research purposes.

## Author
[Ye Min Set Ko Ko (Ronald)]

