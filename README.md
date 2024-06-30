# Stock-Price-Prediction
This project leverages machine learning techniques to predict the future movements of the S&P 500 index based on historical data. The primary focus is on using a Random Forest Classifier to predict whether the closing price of the S&P 500 index will increase the following day.

## Overview
This project involves:
- Fetching historical S&P 500 data using the `yfinance` library.
- Preparing the data for machine learning.
- Training a Random Forest Classifier to predict the next day's closing price movement.
- Evaluating the model's performance using precision score.
- Backtesting the model to evaluate its performance over a historical period.

## Data Source
The historical data for the S&P 500 index is fetched using the `yfinance` library.


## Model Details
  ### Data Preparation
  - Remove unnecessary columns (`Dividends` and `Stock Splits`).
  - Create a target variable that indicates if the closing price will increase the next day.

  ### Model Training
  - The model is trained using the `RandomForestClassifier` with specific hyperparameters to handle class imbalance.

  ### Evaluation
  - The model's performance is evaluated using the precision score.
  - Class distributions of predictions and actual targets are printed for further insights.

## Backtesting
  ### Functions
  - `predict`: Trains the model and makes predictions.
  - `backtest`: Evaluates the model's performance over a historical period in steps.

### Additional Predictors
- New predictors based on rolling averages and trends over different horizons are added to enhance the model.

### Execution
- The backtest function runs the model over historical data and outputs performance metrics and plots.

## Results
The results include:
- Precision scores for the model on the test set and backtest set.
- Plots comparing predicted and actual targets.
- Distribution of predictions in the backtest period.
