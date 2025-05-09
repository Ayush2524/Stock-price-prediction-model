# Future_ML_01

Data Collection:
  Used yfinance to fetch AAPL stock data from 2012 to 2018.
  Focused on the Close price for prediction.
  
Feature Engineering:
  Created MACD (Moving Average Convergence Divergence) and Signal Line for momentum analysis.
  Calculated Bollinger Bands to assess volatility and price channels.
  
Data Preprocessing:
  Normalized data with StandardScaler.
  Created time-series sequences for LSTM input (60-day lookback).
  Created another model using XGboost, and also using RandomforestClassifier.
  
Model Architecture:
  A deep LSTM neural network with dropout layers to avoid overfitting.
  Compiled using the Adam optimizer and trained on 80/20 split data.
  
Evaluation Metrics:
  Mean Squared Error (MSE)
  Mean Absolute Error (MAE)
  R² Score
  
The model was able to predict trends accurately, though exact prices were slightly smoothed due to normalization.

MACD crossovers were helpful in marking potential buy/sell points.

Bollinger Band squeezes indicated breakout periods with surprising accuracy.

Validation R² Score: ~0.99 (indicating high correlation)

The LSTM and XGboost turn out to be the closest enough to the actual prices trend, though the LSTM being the best.
