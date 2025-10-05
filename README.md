# Quantitative Algorithmic Trading Strategy: MA Crossover vs. Machine Learning

## 🎯 Project Overview (Tailored for Quant Roles)
This project implements and compares two algorithmic trading strategies—a foundational **Moving Average (MA) Crossover** and an advanced **Machine Learning (Random Forest) Classifier**—to generate high-Sharpe-Ratio returns on the S&P 500 ETF (SPY).

The primary focus was to leverage software engineering skills to build robust backtesting infrastructure and develop an algorithm that minimizes drawdown, a critical risk management function.

## 📊 Key Performance Metrics (2020-2024 Backtest)

| Metric | Buy & Hold (Benchmark) | Pure Quant (MA Strategy) | **Quant + ML (Random Forest)** |
| :--- | :--- | :--- | :--- |
| **Annualized Return** | ~9.5% (Approx. Benchmark) | 14.63% | **114.50%** |
| **Sharpe Ratio** | < 1.0 | 1.23 | **8.14** (Exceptional Risk-Adjusted Return) |
| **Max Drawdown (Risk)** | ~25-30% | -13.18% | **-4.42%** (Significantly Lower Risk) |

---

## 💻 Technical Approach

1.  **Data Acquisition:** Utilized the `yfinance` API to fetch daily OHLCV data for the SPY ETF (representing International Capital Markets).
2.  **Feature Engineering:** Built a feature set using core technical indicators (`SMA-50`, `SMA-200`, `RSI`, and **Volatility**) to quantify market state.
3.  **Model:** Implemented a **Random Forest Classifier** to predict the next day's price movement (Up/Down). Crucially, the data was split sequentially (`shuffle=False`) to prevent look-ahead bias.
4.  **Risk Management:** Developed a custom backtesting framework to calculate and prioritize the **Sharpe Ratio** and **Maximum Drawdown**, demonstrating a focus on risk-adjusted returns over simple profit.

## 🛠️ How to Run the Project

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_GITHUB_REPO_URL]
    ```
2.  **Create and Activate Environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # Use .\venv\Scripts\activate on Windows
    ```
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Analysis:** Open the `main_algorithm.ipynb` notebook and run all cells sequentially.

---
