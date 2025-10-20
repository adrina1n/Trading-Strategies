# 📈 Trading Strategies Library

Collection of **algorithmic trading strategies** implemented in Python.  
This repository explores various approaches from **technical analysis** to **machine learning**, all tested through a custom **backtesting framework**.

---

## 🧠 Overview

The goal of this project is to **compare, analyze and optimize** the performance of different trading strategies on historical market data.

Each strategy is built as an independent module and can be tested individually or combined to form hybrid approaches.

---

## ⚙️ Features

- 🧩 Modular structure — each strategy in its own Python file  
- 📊 Backtesting engine to evaluate performance  
- 📈 Built-in metrics: Sharpe ratio, max drawdown, cumulative returns, hit ratio  
- 📉 Strategies included:
  - Moving Average (SMA / EMA / Crossover)
  - RSI (Relative Strength Index)
  - MACD (Moving Average Convergence Divergence)
  - (More coming soon...)

---

## 🧪 Example Usage

```python
from strategies import rsi, macd, moving_average
from backtest import Backtester
import pandas as pd

data = pd.read_csv("data/SPY.csv", index_col="Date", parse_dates=True)
bt = Backtester(data, strategy=rsi.RSIStrategy(period=14, overbought=70, oversold=30))
bt.run()
bt.plot_results()
