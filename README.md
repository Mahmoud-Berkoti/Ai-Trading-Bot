# AI Trading Bot

The AI Trading Bot is a sophisticated automated trading strategy, engineered to leverage sentiment analysis for making insightful trading decisions. This bot incorporates cutting-edge machine learning models and APIs, striving to surpass the performance of major brokerage platforms.

## Features:

- **Automated Trading**: Seamlessly integrates with the Alpaca API and Lumibot for automated trade execution.
- **Sentiment Analysis**: Utilizes FinBERT and PyTorch transformer models to analyze market sentiment effectively.
- **Historical Data Analysis**: Employs YahooDataBacktesting for robust backtesting based on historical data.
- **Real-Time Strategy Execution**: Features a REST API that facilitates real-time strategy execution.

## Setup Instructions

## Cloning the Repository:

```bash
git clone https://github.com/Mahmoud-Berkoti/AI-Trading-Bot.git

cd AI-Trading-Bot
```
## Installing Dependencies:

```bash
pip install alpaca-trade-api lumibot transformers torch
```
## Install the required libraries using pip:

```bash
pip install alpaca-trade-api lumibot transformers torch
```

## Downloading Pre-Trained Models

```python
from transformers import AutoTokenizer, AutoModelForSequenceClassification

tokenizer = AutoTokenizer.from_pretrained("ProsusAI/finbert")
model = AutoModelForSequenceClassification.from_pretrained("ProsusAI/finbert")
```

## Configuration

Set up your Alpaca API keys by replacing the placeholders in the MLTrader class with your personal Alpaca API credentials.

## Running the Strategy

To backtest and run the strategy, use the script below:

```python
from datetime import datetime
from lumibot.brokers import Alpaca
from lumibot.backtesting import YahooDataBacktesting
from your_script import MLTrader

if __name__ == "__main__":
    start_date = datetime(2020, 1, 1)
    end_date = datetime(2024, 7, 23)
    broker = Alpaca(MLTrader.ALPACA_CREDS)
    strategy = MLTrader(name='mlstrat', broker=broker, parameters={"symbol": "SPY", "cash_at_risk": 0.5})
    strategy.backtest(YahooDataBacktesting, start_date, end_date, parameters={"symbol": "SPY", "cash_at_risk": 0.5})
```

```css

This code block represents the entire README, formatted with Markdown syntax, ready to be used in your repository to provide users with a comprehensive guide to setting up and running your AI Trading Bot.

```
