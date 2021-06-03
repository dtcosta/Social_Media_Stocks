# Twitter Stock Screener

+ Summary.
+ Tools used.
+ Description of the data.
+ Links for the code.

## 1. Summary

With the rise in social media influence on stock market returns, I thought it would be interesting to analyze data and see if there is a correlation between frequency of mention and stock price movement. This was achieved by gathering data from the Tweepy Twitter API analyzing 20,000 tweets from various finance gurus and influencers within a week timeframe. With the data gathered, tickers were counted to find the most discussed. Next, correlation of high Twitter mentions and positive performance was analyzed.

Top Tickers:

<img src ="Pictures/ticker_symbols.png" alt="twitter" width="300"/>

## 2. Tools used

<img src ="Pictures/twitter_bird.png" alt="twitter" width="300"/>

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
from tweepy import OAuthHandler
import alpaca_trade_api as tradeapi
from MCForecastTools import MCSimulation
#from dotenv import load_dotenv
from textblob import TextBlob
```

## 3. Description of the data.

<img src ="Pictures/twitter_stock_influencers.jpg" alt="twitter" width="300"/>

The data from the Project was fetched from the Tweepy Twitter API. It compiled tweets from the curated list of 100 different finance gurus and influencers. 

Financial data was received from yfinance. The information being fetched from each ticker is the Open, High, Low, Close, Adj Close and Volume.

## 4. Link to our code.

* [Notebook of the code](DEGA.ipynb)
* [DEGA tool- a tool to save tweets](DEGA_TOOL.ipynb)



