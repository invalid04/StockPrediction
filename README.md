# Stock Prediction Model

## Overview

This project demonstrates a stock prediction model that forecasts the movement of the S&P 500 index using historical data and machine learning techniques. The project utilizes various Python libraries for data handling, analysis, and modeling within a Jupyter Notebook environment.

## Tools and Libraries Used

1. **Jupyter Notebook**: An interactive computing environment that allows you to create and share documents containing live code, equations, visualizations, and narrative text.
2. **yfinance**: A Python library for accessing financial data from Yahoo Finance. It was used to fetch historical data of the S&P 500 index.
3. **pandas**: A powerful data manipulation and analysis library for Python. It was used for data cleaning, manipulation, and visualization.
4. **scikit-learn**: A machine learning library for Python. It was utilized to implement and evaluate the Random Forest Classifier model.

## Data

The historical data for the S&P 500 index was retrieved using the `yfinance` library. The data includes daily open, high, low, close prices, and trading volumes. The dataset spans from the earliest available date to the current date.

## Data Processing and Features

1. **Data Cleaning**: The data was filtered to include records from January 1, 1990, onwards to ensure a more recent and relevant dataset.
2. **Feature Engineering**:
   - **Tomorrow’s Price**: Created by shifting the 'Close' price by one day.
   - **Target Variable**: A binary variable indicating whether the next day's closing price is higher than the current day's closing price.
   - **Rolling Averages and Trends**: Calculated rolling averages for various horizons and derived new predictors such as the ratio of the closing price to its rolling average and the sum of target values over the rolling horizon.

## Model

The primary model used in this project is the **Random Forest Classifier**, implemented using `scikit-learn`. Key steps include:
1. **Model Training**: The model was trained on the historical data using features like 'Close', 'Volume', 'Open', 'High', and 'Low' prices.
2. **Prediction and Evaluation**: The model’s predictions were evaluated using precision scores. The backtesting function was used to validate the model's performance over time.

## Results

- The model's predictions were visualized and evaluated for accuracy using precision scores.
- Additional predictors based on rolling averages and trends were tested to improve the model's performance.

## Conclusion

This project highlights the use of machine learning for stock price prediction. While the model provides a basic framework, its performance could be enhanced by incorporating more sophisticated features and techniques.

For further details and to view the complete code, please refer to the [Jupyter Notebook](https://nbviewer.org/github/invalid04/StockPrediction/blob/main/stockPredictionModel.ipynb).
