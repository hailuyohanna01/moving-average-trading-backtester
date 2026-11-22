# Moving-Average Trading Strategy Backtester

## Project Overview

This project develops a Python-based backtesting framework to evaluate a moving-average crossover trading strategy using historical SPY ETF market data.

The objective is to compare the strategy's historical performance against a passive buy-and-hold benchmark while analyzing transaction costs, volatility, maximum drawdown, and risk-adjusted returns.

## Technologies

- Python
- pandas
- NumPy
- Matplotlib
- yfinance
- Google Colab

## Methodology

**1. Historical Market Data**

Download SPY adjusted daily closing prices from January 2020 through December 2025.

**2. Trading Strategy**

Calculate 20-day and 50-day simple moving averages.

- Hold SPY when the 20-day moving average exceeds the 50-day moving average.
- Otherwise, hold cash.
- Shift trading signals by one trading day to avoid using current-day closing information to earn current-day returns.

**3. Backtesting**

Simulate an initial $10,000 investment and compare cumulative returns against buying and holding SPY.

**4. Transaction Costs**

Apply an illustrative 0.05% proportional cost when switching between SPY and cash.

**5. Risk Analysis**

Evaluate total return, annualized volatility, maximum drawdown, and Sharpe ratio.

## Results

Results will be added after completing and validating the backtest.

## Model Validation

The project includes tests for valid trading signals, lagged position calculations, return consistency, transaction-cost effects, and positive portfolio values.

## Limitations

- Historical performance does not guarantee future returns.
- Trading costs are simplified assumptions rather than observed execution costs.
- Cash is assumed to earn no interest.
- The backtest does not model taxes or market impact.
- Daily close-to-close returns simplify actual order execution.
- The moving-average parameters have not undergone rigorous independent out-of-sample validation.

## Future Improvements

- Compare additional moving-average windows.
- Introduce interest earned on cash.
- Implement explicit next-open execution assumptions.
- Conduct walk-forward testing.
- Compare risk-adjusted performance across different market environments.

## Conclusion

This project demonstrates the development, evaluation, and validation of a rule-based trading strategy using Python and historical financial market data.
