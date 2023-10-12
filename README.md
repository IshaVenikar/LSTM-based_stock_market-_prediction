A stock price prediction model using of an LSTM model. The stock prices are predicted on the basis of past information. LSTM is an ideal technique for stock market prediction due to its dynamic as well as complex nature. In particular, Stacked LSTM are employed for the prediction because they utilize the historic or time-series data, making it capable of learning long term dependencies in the data and therefore making the predictions more accurate.  After training the model the stock prices for the next 30 days were forecasted.

![image](https://github.com/IshaVenikar/LSTM-based_stock_market-_prediction/assets/145848618/8b97dd46-6768-497a-a0f5-dc44603b983c)

Figure 1 - Flow chart of the Prediction model

1. Collect stock data- 
Pandas_datareader library will be used for data collection. In order to get stock market data, Tiingo has been used. Tiingo, which is a financial data platform which makes high- quality financial tools obtainable to everyone. The apple stock market dataset(AAPL) has been used.

2. Pre-processing-
Field Selection: Out of all the fields present, such as low, high, open ,close etc, we will select one to visualize the stock price changes. The selected field is the close price of that  stock.

3. Scaling-
LSTM is scale-sensitive. Therefore the values in the dataset are scaled down to values between 0-1 using minmax scaler. 

4. Train-Test Split-
The training size is 65% of the total dataset and testing size of 35%.

5. Building the LSTM model-
Since the data we are working with is “Time series data”, the next value is dependent on the previous values. 
We can say that day 2 is dependent on day 1 and day 3 on day 1 and 2 and so on. 
Timesteps - to compute output of the next day how many previous days output should be considered(3)
For this project we have considered 100 timesteps. Therefore 100 values will be appended into our x_train and in the y_train we will have 1 value. Similarly for x_test and y_text.

7. Predict the test data and check its accuracy. Predict the test data by making use of the built model and then the predicted values are plotted to visualize the accuracy of the model.

8. Predict the next 30 days stock prices using our model- Using the model, the prediction of the stock prices for the next 30 days would be done thereby plotting the predicted output.

