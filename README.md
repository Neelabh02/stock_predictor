# End-to-End Stock Market Forecasting System

Live Demo:
https://stock-predictor-o3ym.onrender.com/


## Problem Statement
Stock market prediction is a complex task due to its dynamic and non-linear behavior. 
This project aims to build an end-to-end deep learning-based system that predicts stock prices using historical data and visualizes trends through an interactive web application.

## Objective
- To analyze historical stock price data
- To predict future stock prices using deep learning (LSTM)
- To visualize stock trends using moving averages
- To deploy an interactive web application using Streamlit

## 🛠️ Tech Stack

### Language
- Python

### Libraries
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Keras / TensorFlow
- yfinance

### Framework
- Streamlit

### Deployment
- Render

## Data Collection
- Historical stock data is fetched using the Yahoo Finance API (yfinance)
- Data range: 2015 to 2025
- Features used:
  - Closing Price
- Data is time-series and indexed by date

## Data Preprocessing
- Extracted closing price for prediction
- Split data into 80% training and 20% testing
- Applied MinMaxScaler for normalization (range: 0 to 1)
- Used last 100 days of data to create sequences (sliding window)
- Reshaped data into 3D format for LSTM input

## Model Used
- Implemented Long Short-Term Memory (LSTM) network for time-series forecasting
- LSTM is used because it can capture long-term dependencies in sequential data
- The model takes the previous 100 days of stock prices to predict the next value
- Pre-trained model is loaded using Keras (.keras file)

## Evaluation Metrics
- Model performance is evaluated using:
  - Mean Squared Error (MSE)
  - Visual comparison of predicted vs actual prices

## Prediction Logic
- The model uses the last 100 days of stock prices as input
- Predicts the next day's stock price
- Predictions are rescaled back to original values using inverse scaling
https://stock-predictor-o3ym.onrender.com/

## Deployment
- Built an interactive web application using Streamlit
- Integrated trained LSTM model into the application
- Deployed on Render for public access
