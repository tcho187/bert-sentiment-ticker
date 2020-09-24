# bert-sentiment-ticker
Analysis on stock ticker prices after earnings call


Scraped over X earning call transcripts from The Motley Fool using python and selenium

Sentiment Analysis using FinBert https://github.com/ProsusAI/finBERT


Got ticker prices, industry, eps from Finnhub API https://github.com/Finnhub-Stock-API/finnhub-python


Ran inferential statistics (Chi Square test of independence, one way ANOVA)

https://nbviewer.jupyter.org/github/tcho187/bert-sentiment-ticker/blob/master/bert%20sentiment%20for%20tickers.ipynb



# Code and Resources Used

Python Version: 3.7

Packages: pandas, numpy, finnhub, plotly, nltk, selenium, bs4

# Web Scraping

Tweaked the web scraper github repo (above) to scrape 1000 job postings from glassdoor.com. With each job, we got the following:

- Ticker

- Company Name

- Date of Earnings Call

- Time of Earnings Call

- Stock Exchange

- Prepared Remarks

- Date of Earnings Quarter

# Sentiment Prediction

FinBERT is a language model that further pre trains from BERT using subset of Reuters TRC2 dataset. FinBERT is fine tuned for text classification using Financial Phrase Bank. I feed the earnings call transcript through FinBERT to predict the sentiment of the sentences.

# Financial API

I use Finnhub API to retrieve the following:

- Opening Price of day before earnings call

- Closing Price of day before earnings call

- High Price of day before earnings call

- Low Price of day before earnings call

- Volume of day before earnings call


- Opening Price of day during/after earnings call

- Closing Price of day during/after earnings call

- High Price of day during/after earnings call

- Low Price of day during/after earnings call

- Volume of day during/after earnings call

- EPS (Earnings per Share)

- Industry
