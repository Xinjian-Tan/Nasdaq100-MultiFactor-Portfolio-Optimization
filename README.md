# Nasdaq100-MultiFactor-Portfolio-Optimization

This is a quantitative investment research project combining multi-factor stock selection, portfolio optimization, and backtesting on Nasdaq-100 constituents.

## Overview

This project develops a systematic quantitative investment framework for selecting and allocating capital among companies in the Nasdaq-100 Index.

Rather than relying on a single indicator or discretionary stock-picking approach, the framework combines:

* Historical market data
* Fundamental financial data
* Multi-factor stock selection
* Top-25 portfolio construction
* Mean-variance portfolio optimization
* Minimum-volatility portfolio construction
* Maximum-Sharpe portfolio construction
* Historical backtesting
* Portfolio performance and risk analysis

## Objective

To construct portfolios from Nasdaq-100 constituents by using muti-factor model [ with backtest ]

## Stock Selection

The model ranks all eligible constituents and selects the Top 25 stocks based on their aggregate factor scores.

## Portfolio Construction

### Minimum-Risk Portfolio

### Maximum-Sharpe Ratio Portfolio

The resulting portfolios are then evaluated through historical backtesting.

## About our Muti-factor

### Momentum

`0.3*Z(3M Return) + 0.3*Z(6M Return) + 0.4*Z(12-1M Return)`

### Value

`0.3*Z(FCF Yield) + 0.3*Z(Earnings Yield) + 0.4*Z(EBITDA/EV)`

### Quality

`0.35*Z(ROIC) + 0.25*Z(Operating Margin) + 0.20*Z(FCF Margin) - 0.20*Z(Net Debt/EBITDA)`

### Growth

`0.4*Z(3Y Revenue CAGR) + 0.4*Z(3Y EPS CAGR) + 0.2*Z(3Y FCF CAGR)`

### Low Volatility

`-0.6*Z(60D Volatility) - 0.4*Z(252D Volatility)`

### Liquidity

`0.7*Z(log(20D ADV)) + 0.3*Z(log(60D ADV))`
