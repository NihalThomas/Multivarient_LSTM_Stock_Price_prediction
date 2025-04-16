# Multivariate LSTM Stock Price Prediction Model

## Overview
This project implements a multivariate Long Short-Term Memory (LSTM) neural network for stock price forecasting, designed to capture complex temporal patterns in financial time-series data. The model leverages multiple input features to predict future stock prices, with a focus on robust feature engineering for trading applications.

## Model Architecture
The model consists of a deep LSTM architecture:
- **Three LSTM Layers**: Two layers with 100 units each (return sequences enabled) and a final layer with 50 units, capturing long-term dependencies.
- **Batch Normalization**: Applied after each LSTM layer to stabilize training and improve convergence.
- **Dropout (0.3)**: Added after each LSTM layer to prevent overfitting.
- **Dense Layers**: A 50-unit ReLU-activated layer followed by a single-unit output layer for predicting the next day’s stock price.

## Features
- **Input Features**:
  - Stock data: Open, High, Low, Close, Volume.
  - Technical indicators: 14-day Relative Strength Index (RSI), 20-day and 50-day Simple Moving Averages (SMA).
  - External market data: S&P 500 index Close price.
- **Lookback Period**: 120 days to capture historical trends and patterns.
- **Data Source**: Historical stock and market data retrieved via the yFinance API.

## Technologies
- **Python**: Core programming language.
- **TensorFlow/Keras**: For building and training the LSTM model.
- **NumPy/Pandas**: For data preprocessing and feature engineering.
- **yFinance API**: For fetching stock and market data.
- **Scikit-Learn**: For data normalization and evaluation metrics.

## Purpose
The model is designed for time-series forecasting of stock prices, enabling quantitative analysis and trading strategy development by integrating diverse financial indicators and market signals.
