
<img src ="Photos/twitter_stock_influencers.jpg" alt="twitter" width="750"/>

# Twitter Stock Screener

+ Summary
+ Tools used
+ Results 

## 1. Summary

With the rise in social media influence on stock market returns, I thought it would be interesting to analyze data and see if there is a correlation between frequency of mention and stock price movement. This was achieved by gathering data from the Tweepy Twitter API analyzing 20,000 tweets from various finance gurus and influencers within a week timeframe. With the data gathered, tickers were counted to find the most discussed. 

Top Tickers:

<img src ="Photos/tickers_symbols.png" alt="twitter" width="250"/>

## 2. Tools used

<img src ="Photos/twitter_bird.png" alt="twitter" width="750"/>

In order to run the notebook, you will need a Twitter developer account. After being approved, consumer keys, consumer_secrets, access_token and access_token_secret to access the API will be provided. Here is a link to help you start learning about the Twitter API, [Twitter Starter Guide.](https://developer.twitter.com/en/docs/twitter-api/getting-started/guide)

Once you have the keys, you must create a file called API.env on the same folder you are running the notebook with the following:

```
consumer_keys = "Enter it here"
consumer_secrets = "Enter it here"
access_token = "Enter it here"
access_token_secret = "Enter it here"
```

Python package downloads:

```
pip install tweepy
pip install yfinance 
pip install -U python-dotenv
pip install -U textblob
pip install seaborn
pip install matplotlib.pyplot
pip install regex
pip install requests
pip install datetime
pip install alpaca-trade-api
pip install pandas
```

Imports:
```
import tweepy
import pandas as pd
import re
import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import datetime
import time
import requests
import os
import plotly.graph_objects as go
from tweepy import OAuthHandler
import alpaca_trade_api as tradeapi
#from dotenv import load_dotenv
from textblob import TextBlob
```

## 3. Description of the data.

I decided to remove SPY and QQQ ETF from the results and built an equally weighted portfolio of the remaining top five stocks. 

<img src ="Photos/newplot%20(10).png" alt="portfolio" width="850"/>


Financial data was received from yfinance. The information being fetched from each ticker is the Open, High, Low, Close, Adj Close and Volume. I then used Plotly to visualize the returns of the 5 stock portfolio versus a benchmark starting on March 1, 2021 through June 30, 2021. 

<img src ="Photos/newplot%20(11).png" alt="portfolio" width="950"/>



