# Stock Trader AI

A reinforcement learning agent that learns profitable stock trading strategies from real market data and social media sentiment. Uses **Proximal Policy Optimization (PPO)** with a custom [Gymnasium](https://gymnasium.farama.org/) environment to manage a portfolio of 13 US stocks, outperforming a buy-and-hold baseline by **4.6%** over the six-week test period.

See [the project report](report.pdf) for full methodology and results.

---

## Datasets

- **Stock prices**: [USA Stocks OHLCV](https://www.kaggle.com/datasets/olegshpagin/usa-stocks-prices-ohlcv) — hourly data for 514 US stocks (1998–2024)
- **Tweets**: [Stock Tweets for Sentiment Analysis](https://www.kaggle.com/datasets/equinxx/stock-tweets-for-sentiment-analysis-and-prediction) — ~65k tweets for 25 companies (Sep 2021–Sep 2022)
- **Risk-free rate**: [3-Month Treasury Bill Yield (DTB3)](https://fred.stlouisfed.org/series/DTB3)

---

## Tech Stack

- Python 3.14
- [Stable Baselines3](https://stable-baselines3.readthedocs.io/) (PPO)
- [Gymnasium](https://gymnasium.farama.org/) (custom environment)
- scikit-learn, pandas, numpy, matplotlib
- HuggingFace Transformers (sentiment model)

---

## Running the Demo

```bash
pip install -r requirements.txt
```

Open `project.ipynb` and run all cells **in order**, running each cell **only once**. Restart the kernel and run from the top if anything goes wrong.

---

## Repository Structure

```
project.ipynb                  # Demo: pretrained models on test data
project.html                   # HTML export of the demo notebook
report.pdf                     # Full project report
requirements.txt               # Python dependencies
src/
├── StockTrader.ipynb          # Custom Gym environment, training, and evaluation
├── stock_clustering.ipynb     # Hierarchical clustering of stocks by price trajectory
├── preprocessing.ipynb        # Sentiment + stock + risk-free rate preprocessing
├── pretrained_models/         # Saved PPO models trained on each cluster
├── sentiment_stock_data/      # Preprocessed stock + sentiment CSVs
├── stock_data/                # Raw hourly stock price data
├── DTB3.csv                   # Raw risk-free rate data
├── risk_free_rates.csv        # Cleaned risk-free rates for Sharpe ratio
└── stock_tweets.csv           # Stock-related tweets dataset
```
