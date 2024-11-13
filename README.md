The AI Trading Bot is an automated trading strategy that uses sentiment analysis to make informed trading decisions. Leveraging advanced machine learning models and APIs, it aims to outperform major brokerages.

Features

Automated trading using Alpaca API and Lumibot
Sentiment analysis with FinBERT and PyTorch transformer models
Historical data analysis with YahooDataBacktesting
REST API for real-time strategy execution
Setup Instructions:

Clone the repository: git clone https://github.com/yourusername/https://github.com/Mahmoud-Berkoti/AI-Trading-Bot.git cd AI-Trading-Bot

Install required libraries: pip install alpaca-trade-api lumibot transformers torch

Download pre-trained models: from transformers import AutoTokenizer, AutoModelForSequenceClassification tokenizer = AutoTokenizer.from_pretrained("ProsusAI/finbert") model = AutoModelForSequenceClassification.from_pretrained("ProsusAI/finbert")

Set up your Alpaca API keys: Replace the placeholders in the MLTrader class with your Alpaca API credentials

Running the Strategy To backtest and run the strategy, run the following script: from datetime import datetime from lumibot.brokers import Alpaca from lumibot.backtesting import YahooDataBacktesting from your_script import MLTrader

if name == "main": start_date = datetime(2020, 1, 1) end_date = datetime(2024, 7, 23) broker = Alpaca(MLTrader.ALPACA_CREDS) strategy = MLTrader(name='mlstrat', broker=broker, parameters={"symbol": "SPY", "cash_at_risk": 0.5}) strategy.backtest(YahooDataBacktesting, start_date, end_date, parameters={"symbol": "SPY", "cash_at_risk": 0.5})
