# Stock-price-prediction-with-Time-series-FBprophet-
Time Series Analysis in Python

Goal is to predict the range of reliance stock price till 2020.

First, we import the required libraries and get some data. 

Quandl automatically puts our data into a pandas dataframe, the data structure of choice for data science.

fbprophetis designed for analyzing time series with daily observations that display patterns on different time scales. It also has advanced capabilities for modeling the effects of holidays on a time-series and implementing custom changepoints, but we will stick to the basic functions to get a model up and running. Prophet, like quandl, can be installed with pip from the command line.

Steps:
1. Import the required packages
2. load the reliance stock data from quandl with the token they provide
3. visualize the data
4. Build the model based on close value in the dataset
5. Change the year variable as ds and close as y for the sake of fbprophet
6. Build the model with et the changepoint prior to 0.15, up from the default value of 0.05. This hyperparameter is used to control how sensitive the trend is to changes, with a higher value being more sensitive and a lower value less sensitive
7. Make a future dataframe for 2 years
8. Make predictions and plot the forecast

In the plot The black dots represent the actual values (notice how they stop at the beginning of 2018), the blue line indicates the forecasted values, and the light blue shaded region is the uncertainty (always a critical part of any prediction). The region of uncertainty increases the further out in the future the prediction is made because initial uncertainty propagates and grows over time. This is observed in weather forecasts which get less accurate the further out in time they are made.
