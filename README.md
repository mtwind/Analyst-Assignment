# Analyst Trading Strategy

## Overview

This project outlines a trading strategy that combines the Parabolic Stop and Reverse (PSAR) and the Relative Strength Index (RSI) indicators. This strategy aims to produce favorable returns over a 3-5 year period by leveraging these two relatively long-term indicators. The strategy has demonstrated the potential for returns of up to 70% in certain market conditions, with a Sharpe Ratio of 2.7.

## Strategy Implementation Steps

1. Clean Stock Data
2. Implement Parabolic SAR strategy
3. Implement the Relative Strength Index (RSI)
4. Find signals supported by both indicators
5. Calculate Returns
6. Plot data and returns
7. Backtest all data
8. Determine strategy effectiveness using the Sharpe Ratio and Information Ratio

## Technical Indicators

### Parabolic Stop and Reverse (PSAR)

The PSAR indicator is used to determine the direction of the trend and identify potential price reversals.

- **Variables Used:**
  - Extreme Point (EP): The highest or lowest price in the current trend.
  - Acceleration Factor (AF): A value that increases with the trend, affecting the sensitivity of the PSAR.
  - Rising PSAR (RPSAR): The calculated SAR value for an uptrend.
  - Falling PSAR (FPSAR): The calculated SAR value for a downtrend.

![PSAR](/images/PSAR.png)

### Relative Strength Index (RSI)

The RSI is a momentum oscillator that measures the speed and magnitude of a security's recent price changes to evaluate overbought or oversold conditions.

- **Variables Used:**
  - Average Gain: The average of price increases over a specific period.
  - Average Loss: The average of price decreases over a specific period.

![RSI](/images/RSI.png)

## Signal Generation and Returns

### Determining Signals

The strategy generates buy and sell signals by identifying points where both the PSAR and RSI indicators provide corroborating signals.

- **Buy Signal:** Occurs when there is a PSAR buy signal, and the RSI indicates the stock is oversold (typically below 30).
- **Sell Signal:** Occurs when there is a PSAR sell signal, and the RSI indicates the stock is overbought (typically above 70).

### Calculating Returns

The strategy's performance is evaluated by calculating the portfolio's value over time based on the generated buy and sell signals.

## Backtesting and Effectiveness

The strategy was backtested on various tickers, including AMZN, TSLA, and GOOGL, over a four-year period from January 1, 2020, to January 1, 2024.

![Backtesting](/images/backtesting.png)

### Strategy Effectiveness Metrics

The effectiveness of the strategy is measured using the following financial ratios:

- **Sharpe Ratio:** This ratio measures the strategy's risk-adjusted return. It is calculated based on the average returns, the risk-free rate (assumed to be 2%), and the standard deviation of the returns.
- **Information Ratio:** This ratio assesses the portfolio's returns beyond those of a benchmark (in this case, the S&P 500) relative to the volatility of those returns.

### Backtesting Results

The backtesting on AMZN, TSLA, and GOOGL produced the following results:

- **AMZN**:
  - Sharpe Ratio: 2.31
  - Information Ratio: 2.31
- **TSLA**:
  - Sharpe Ratio: 2.10
  - Information Ratio: 2.10
- **GOOGL**:
  - Sharpe Ratio: 1.41
  - Information Ratio: 1.41
