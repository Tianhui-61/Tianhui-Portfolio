# Statistical Arbitrage Strategy Research

## Project overview

This project designs and evaluates a market-neutral pairs-trading strategy using U.S. equity data from 2018 to 2025. The workflow covers data collection, pair screening, dynamic hedge-ratio estimation, signal generation and a strict out-of-sample backtest.

## Research workflow

1. Collected and quality-checked daily split-adjusted closing prices and volume data.
2. Screened candidate pairs using return correlation, Engle-Granger cointegration and mean-reversion diagnostics.
3. Selected CVX-COP and PEP-GIS for further research.
4. Applied a Kalman Filter to estimate time-varying hedge ratios and dynamic spreads.
5. Generated Z-score-based entry, exit and stop-loss signals without look-ahead bias.
6. Backtested the strategy out of sample from 2023 to 2025 with next-trading-day execution, daily rebalancing and transaction costs.

## Out-of-sample findings

At the 10 bps baseline cost assumption, the portfolio generated:

- Total net return: **-7.94%**
- CAGR: **-2.73%**
- Sharpe ratio: **-0.78**
- Maximum drawdown: **-10.70%**
- Completed trades: **37**
- Trade win rate: **48.65%**

The no-cost return remained negative at approximately -4.46%. Mean-reversion exits were gross positive but highly cost-sensitive, while four stopped trades produced the largest losses. The strategy was therefore rejected at the baseline assumptions.

## Skills demonstrated

- Python and Pandas
- Time-series analysis
- Engle-Granger cointegration
- Kalman Filter and dynamic hedge ratios
- Event-driven signal design
- Out-of-sample backtesting
- Transaction-cost and risk analysis
- Reproducible research and model validation

## Project files

- `statistical_arbitrage_phase4_backtest.xlsx`: formula-driven backtest workbook and dashboard
- `statistical_arbitrage_phase4_project.zip`: complete reproducible project package

## Important limitation

The analysis uses split-adjusted closing prices rather than dividend-reinvested total returns. Dividends, short-borrow fees, taxes and market impact are not modeled. The next-close execution convention is deliberately conservative, and no Phase 4 parameter was optimized on out-of-sample profitability.
