# Future Stock Price Prediction
 Predict future stock price of some tickers for the next N days

## Idea
The idea of this prediction is, the model will use the last 100 close price to predict the next day's close price. And to predict the next 2 day close price, I will use the predict of next day's close price and 99 last close price. I use the sliding window algorithm to do this. So, in this kernel, I choose LSTM model to predict future stock price. With this idea, the LSTM model is the most suitable.

With the dataset, the last 60 days is used for testing, and the others is for training. Because of predicting close price of future days, so I just need only past close price, and will not use other features.

## Data description
In this repository, I have 4 file excel data, which are the stock price record of 4 tickers. In each file, it has 8 features: Ticker, Date/Time, Open, High, Low, Close, Volume, Open Interest.  But, I think that, to predict the future stock price - the close price of ticker in the future, we need only previous close price.