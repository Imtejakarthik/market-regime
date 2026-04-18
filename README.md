# 📈 Monte Carlo Option Pricing Simulator

> A professional-grade simulator for pricing European options using Monte Carlo methods, Geometric Brownian Motion, and Black-Scholes analytics — built for finance, education, and research.

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Finance](https://img.shields.io/badge/Domain-Quantitative%20Finance-orange?style=flat-square)

---

## 🧠 What Is This?

This project simulates thousands of stock price paths using **Geometric Brownian Motion (GBM)** and uses them to price **European Call and Put options** via Monte Carlo simulation. Results are cross-validated against the analytical **Black-Scholes formula**, and visualized with animated, professional dark-themed plots.

Whether you're a quant, a student, or a researcher — this tool gives you a clear, hands-on understanding of option pricing under stochastic dynamics.

---

## ✨ Features

- 📊 Simulate stock price paths using Geometric Brownian Motion
- 💰 Price European Call and Put options via Monte Carlo
- 📐 Calculate Black-Scholes analytical prices for comparison
- 🎞️ Animated visualizations of simulated price paths
- 🌙 Clean, professional dark-themed plots
- 🔁 Easy parameter customization (strike, volatility, rate, maturity)

---

## 📁 Project Structure

```
monte-carlo-options/
├── main.py           # Entry point: simulation, visualization, comparison
├── utils.py          # GBM simulation & option pricing functions
├── requirements.txt  # Python dependencies
└── README.md         # You are here
```

---

## 🔢 Mathematical Formulas

### Geometric Brownian Motion (GBM)

Stock price evolution is modeled as:

$$S_t = S_0 \exp\left((r - 0.5\sigma^2)t + \sigma W_t\right)$$

| Symbol | Description |
|--------|-------------|
| $S_t$ | Stock price at time $t$ |
| $S_0$ | Initial stock price |
| $r$ | Risk-free rate |
| $\sigma$ | Volatility |
| $W_t$ | Wiener process (Brownian motion) |

---

### Black-Scholes Formula

**European Call:**
$$C = S_0 N(d_1) - K e^{-rt} N(d_2)$$

**European Put:**
$$P = K e^{-rt} N(-d_2) - S_0 N(-d_1)$$

Where:

$$d_1 = \frac{\ln(S_0/K) + (r + 0.5\sigma^2)t}{\sigma\sqrt{t}}, \qquad d_2 = d_1 - \sigma\sqrt{t}$$

| Symbol | Description |
|--------|-------------|
| $N(\cdot)$ | Cumulative standard normal CDF |
| $K$ | Strike price |
| $t$ | Time to maturity (in years) |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/tubakhxn/monte-carlo-options.git
cd monte-carlo-options
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Simulator

```bash
python main.py
```

---

## ⚙️ Parameters

All parameters are configurable and labeled in the output visualization:

| Parameter | Description | Example |
|-----------|-------------|---------|
| `S0` | Initial stock price | `100` |
| `K` | Strike price | `105` |
| `r` | Risk-free interest rate | `0.05` |
| `sigma` | Volatility (annualized) | `0.2` |
| `T` | Time to maturity (years) | `1.0` |
| `n_paths` | Number of Monte Carlo paths | `10000` |

---

## 📷 Sample Output

The simulator produces an animated plot showing:
- Simulated GBM price paths
- Estimated Monte Carlo option price
- Black-Scholes analytical benchmark
- Market regime overlays (Bull / Bear / Sideways)

---

## 🧪 How It Works

1. **Simulate** — Generate `n_paths` stock price trajectories using discretized GBM
2. **Price** — Average the discounted payoffs across all paths to estimate option price
3. **Compare** — Benchmark against the closed-form Black-Scholes result
4. **Visualize** — Display animated paths and price convergence

---

## 📦 Requirements

```
numpy
scipy
matplotlib
yfinance
```

Install with:
```bash
pip install -r requirements.txt
```

---

## 👤 Author

**tubakhxn**  
Built with ❤️ for quantitative finance education and research.


---

## 🌟 Support

If you found this useful, consider ⭐ starring the repo and sharing it with others interested in quantitative finance!
