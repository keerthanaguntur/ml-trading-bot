# MLTradingBot

## Overview

MLTradingBot is an automated trading bot that leverages machine learning for sentiment analysis of financial news to make real-time trading decisions. The bot uses the FinBERT model, which is specialized in financial sentiment analysis, and integrates with the Alpaca trading API to execute trades on the stock market based on the sentiment derived from news articles.

## Features

- **Sentiment Analysis**: Uses FinBERT to analyze the sentiment of financial news articles (positive, negative, neutral).
- **Automated Trading**: Automatically executes buy, sell, or hold decisions based on sentiment analysis.
- **Real-time News Monitoring**: Continuously monitors and analyzes news to make timely trading decisions.
- **Alpaca API Integration**: Seamlessly connects with the Alpaca trading platform to place trades.

## Installation

### Prerequisites

- Python 3.7+
- An Alpaca account with API keys (for trading execution)
- Basic knowledge of Python and command-line operations

### Setup

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/nicknochnack/MLTradingBot.git
    cd MLTradingBot
    ```

2. **Create a Virtual Environment**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set Up Alpaca API Keys**:
   - Obtain your Alpaca API key and secret from your [Alpaca dashboard](https://alpaca.markets/).
   - Create a `.env` file in the project root directory and add your Alpaca credentials:
     ```
     ALPACA_API_KEY=your_api_key
     ALPACA_SECRET_KEY=your_secret_key
     ALPACA_BASE_URL=https://paper-api.alpaca.markets
     ```

## Usage

1. **Run the Bot**:
   - After setting up the environment and dependencies, run the bot using:
   ```bash
   python tradingbot.py
Bot Workflow:
The bot will start monitoring live financial news.
It will analyze each news article's sentiment using the FinBERT model.
Based on the sentiment score, the bot will decide whether to buy, sell, or hold a particular stock and execute the trade through the Alpaca API.
Project Structure
tradingbot.py: The main script that runs the trading bot, handling news fetching, sentiment analysis, and trade execution.
finbert_utils.py: Contains utility functions for loading the FinBERT model and performing sentiment analysis.
requirements.txt: Lists all Python dependencies required to run the project.
FinBERT Model
FinBERT is a BERT-based model fine-tuned for financial sentiment analysis. It is particularly effective in analyzing the sentiment of financial news articles, which is crucial for making informed trading decisions.

Considerations
Real-time Trading Risks: The bot's performance is highly dependent on the accuracy of sentiment analysis and the timely execution of trades.
Market Volatility: Financial markets can be unpredictable, and relying solely on sentiment analysis may not always yield profitable results. It is recommended to combine this strategy with other risk management tools.
Future Enhancements
Additional Data Sources: Incorporate social media sentiment, stock price trends, and other financial indicators.
Risk Management: Implement stop-loss mechanisms and other risk management strategies.
Model Improvements: Fine-tune the FinBERT model or explore other models to enhance sentiment analysis accuracy.
