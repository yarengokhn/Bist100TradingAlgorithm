## BIST 100 Stock Price Prediction Project

This project utilizes machine learning models to forecast the prices of various stocks listed in the Borsa Istanbul (BIST) 100 index, Turkey's leading stock exchange. 
Project aims to predict the direction of the next candlestick (increase or decrease) for stocks listed in the BIST 100 index of Borsa İstanbul using daily and hourly candlestick charts. A series of features are obtained for each stock by utilizing technical indicators, and these features are fed into machine learning models.

## Data Collection and Preprocessing

The data used in the project is obtained through the Yahoo Finance API. The project retrieves daily price data for each stock within a specified start and end date range. The data utilizes the pandas-ta library to calculate various technical analysis indicators (e.g., moving averages, Bollinger Bands, RSI). Additionally, Min-Max scaling is applied for feature scaling during the data preprocessing step.

## Machine Learning Models

The project employs various machine learning models for stock price prediction. These models include:

- XGBoost: This model is a variant of the Gradient Boosting algorithm and is particularly effective for classification problems.
- CatBoost: Another Gradient Boosting model that handles categorical variables well.
- Random Forest: A model composed of multiple decision trees.
- LightGBM: A fast and high-performance Gradient Boosting model with low memory usage.
- LSTM (Long Short-Term Memory): This model is a type of artificial neural network that is effective for time series data.

Each model takes the selected technical indicators as input and is trained to predict price movements.

## Next Candlestick Prediction

The top 10 stocks are determined by evaluating the F1 scores of different models, and the stocks with the highest scores are selected. For the selected stocks, the direction of the next candlestick is predicted by examining the candlestick charts on daily and hourly timeframes.

These predictions are presented for stocks where the model performs best. The accuracy, precision, recall, and F1 score of the predictions are provided as measurements.
