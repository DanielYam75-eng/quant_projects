# Monte Carlo Portfolio Simulation

## Overview

This project implements a Monte Carlo simulation framework to analyze portfolio risk and return profiles. It models the future behavior of a diversified stock portfolio using historical price data and statistical methods to generate probabilistic forecasts of portfolio performance.

## Project Description

The simulation performs the following workflow:

### 1. **Data Acquisition**
- Fetches one year of historical adjusted close prices for five major tech stocks: AAPL, MSFT, GOOGL, AMZN, and META
- Uses the `yfinance` library to retrieve reliable market data from Yahoo Finance

### 2. **Statistical Analysis**
- Calculates daily returns and mean return for each stock
- Computes the covariance matrix to capture correlations between stock movements
- These metrics form the foundation for generating realistic simulated returns

### 3. **Monte Carlo Simulation**
- Generates 100 simulation paths spanning 100 trading days
- Uses Cholesky decomposition to account for correlations between stock returns
- Creates random normal variables to represent market uncertainty
- Applies equal-weight portfolio allocation across all stocks with a $1M initial investment

### 4. **Risk Analytics**
The framework calculates key financial metrics:
- **95% Confidence Interval**: Range of likely final portfolio values
- **Mean Final Value**: Expected portfolio value at simulation end
- **Probability of Profit**: Likelihood portfolio exceeds initial investment
- **Risk Metrics**: Standard deviation, Sharpe ratio, and Conditional Value-at-Risk (CVaR)
- **Expected Shortfall**: Average loss in worst-case 5% scenarios

## Requirements

```
pandas
numpy
yfinance
matplotlib
```

## Usage

Run the Jupyter notebook cells sequentially:

1. **Cell 1**: Data retrieval and statistical computations
2. **Cell 2**: Monte Carlo simulation execution
3. **Cell 3**: Visualization and metrics calculation

The final output displays a portfolio performance chart and comprehensive risk statistics.

## Key Outputs

- Visualization of 100 simulated portfolio paths
- 95% confidence interval for final portfolio value
- Probability of losses or gains
- Risk-adjusted return metrics for portfolio optimization

## Technologies

- Python 3
- Jupyter Notebook
- NumPy (numerical computations)
- Pandas (data manipulation)
- Matplotlib (visualization)
- yfinance (data retrieval)

## Notes

This simulation uses historical correlations and returns as predictors of future performance. Results should be interpreted as probabilistic scenarios, not predictions.
