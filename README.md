# 📊 Market Regime Switching RL Agent

An adaptive trading bot that combines **Reinforcement Learning (RL)** with **Market Regime Detection** to dynamically switch trading strategies based on changing market conditions like bull, bear, sideways, and high volatility regimes.

---

## 🚀 Overview

Traditional trading systems often fail when market conditions change. This project solves that by:

- Detecting market regimes using **unsupervised learning**
- Training a reinforcement learning agent to adapt to each regime
- Optimizing trading decisions using **risk-adjusted rewards**

---

## 🧠 Key Concepts

- Reinforcement Learning (DQN / PPO)
- Market Regime Detection
- Gaussian Mixture Models (GMM)
- K-Means Clustering
- Sharpe Ratio Optimization

---

## ✨ Features

- 📈 Fetches historical stock data using `yfinance` or CSV
- 🧮 Feature engineering:
  - Returns
  - Rolling volatility
  - Moving averages
  - RSI
- 🧠 Market regime detection:
  - GMM or KMeans clustering
- 🤖 RL agent:
  - DQN or PPO (Stable-Baselines3)
- 🔄 Dynamic strategy switching per regime
- 📊 Visualization:
  - Price charts with regime overlays
  - Buy/sell signals
  - Equity curve

---

## 📁 Project Structure

```bash
Market-Regime-Switching-RL-Agent/
│
├── data.py          # Load historical data
├── features.py      # Feature engineering
├── regime.py        # Market regime detection (GMM/KMeans)
├── env.py           # Custom RL trading environment
├── agent.py        # RL agent (DQN / PPO)
├── train.py        # Training pipeline
├── visualize.py    # Performance visualization
├── requirements.txt
└── README.md

git clone https://github.com/Imtejakarthik/market-regime.git
cd market-regime

pip install -r requirements.txt

▶️ Usage
1. Load Data
python data.py
2. Feature Engineering
python features.py
3. Detect Market Regimes
python regime.py
4. Train RL Agent
python train.py
5. Visualize Results
python visualize.py
📊 Output
Trained RL trading model
Market regime classification
Performance metrics:
Sharpe Ratio
Drawdown
Total Returns
Graphs:
Price + regime visualization
Trading signals
Equity curve
📚 References
Reinforcement Learning
Market Regime
Gaussian Mixture Model
K-Means Clustering
Sharpe Ratio
