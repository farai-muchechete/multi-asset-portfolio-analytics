# Multi-Asset Portfolio Analytics Platform

**Python | Portfolio Optimization | Quantitative Risk Management | Monte Carlo Simulation | Backtesting**

## Project Overview

Developed a Python-based multi-asset portfolio analytics platform to evaluate portfolio construction, risk-adjusted performance, downside risk and implementation costs across four investment strategies.

The analysis covers eight exchange-traded funds (ETFs) representing U.S. equities, international equities, emerging markets, fixed income, real estate and gold.

Four portfolio strategies were evaluated:

- Equal Weight
- Minimum Variance
- Maximum Sharpe Ratio
- Risk Parity

## Methodology

- **Data:** Historical adjusted ETF prices from Yahoo Finance, covering 2015–2025.
- **Portfolio optimization:** Long-only portfolio allocations subject to full-investment constraints.
- **Backtesting:** 252-trading-day rolling estimation windows, monthly portfolio rebalancing and out-of-sample evaluation from February 2016 through December 2025.
- **Risk management:** Annualized volatility, Sharpe ratio, historical Value at Risk (VaR), Conditional Value at Risk (CVaR) and maximum drawdown.
- **Monte Carlo simulation:** 10,000 correlated return scenarios over a 252-trading-day horizon.
- **Stress testing:** Hypothetical equity-market, interest-rate and inflation shocks.
- **Implementation analysis:** Portfolio turnover and transaction-cost sensitivity at 5, 10 and 25 basis points per dollar traded.

## Key Results

| Strategy         | Gross Return | Net Return (10 bps) | Volatility | Max Drawdown |
| ---------------- | ------------ | ------------------- | ---------- | ------------ |
| Equal Weight     | 7.89%        | 7.87%               | 9.37%      | -20.74%      |
| Minimum Variance | 1.87%        | 1.86%               | 1.56%      | -6.00%       |
| Maximum Sharpe   | 4.13%        | 3.48%               | 10.90%     | -34.09%      |
| Risk Parity      | 4.97%        | 4.89%               | 5.18%      | -14.87%      |

Returns are annualized. Net returns reflect illustrative transaction costs.

## Key Investment Findings

**1. Equal Weight outperformed optimized strategies.**

The Equal Weight portfolio generated the highest out-of-sample annualized return (7.89%) and Sharpe ratio (0.63), highlighting the potential limitations of optimization based on historical estimates.

**2. Maximum Sharpe exhibited substantial implementation costs.**

The Maximum Sharpe strategy generated 326.54% annualized one-way turnover. Its annualized return declined from 4.13% gross to 3.48% net under the 10-basis-point transaction-cost assumption.

**3. Minimum Variance delivered the strongest downside protection.**

The strategy experienced 1.56% annualized volatility and a maximum historical drawdown of 6.00%, although its return was relatively low.

**4. Risk Parity provided a defensive alternative.**

Risk Parity generated a 4.97% gross annualized return with 5.18% volatility and a maximum drawdown of 14.87%.

## Monte Carlo Simulation

Simulated 10,000 potential one-year return paths for each portfolio using historically estimated mean returns and covariance.

The estimated probabilities of ending below the initial investment were:

| Strategy         | Simulated Probability of Loss |
| ---------------- | ----------------------------- |
| Equal Weight     | 21.60%                        |
| Minimum Variance | 11.62%                        |
| Maximum Sharpe   | 37.83%                        |
| Risk Parity      | 17.60%                        |

## Limitations

The analysis excludes taxes, market impact and financing costs. Transaction costs are modeled using illustrative assumptions. Monte Carlo simulations assume normally distributed returns with fixed historical parameters. Historical and simulated performance do not guarantee future results.

## Technologies

Python, Pandas, NumPy, SciPy, Matplotlib, Jupyter Notebook and Yahoo Finance market data.

## Conclusion

The project demonstrates that sophisticated portfolio optimization does not necessarily outperform simpler allocation strategies out of sample. Robust investment analysis requires evaluating return, volatility, downside exposure, portfolio turnover and transaction costs together.
