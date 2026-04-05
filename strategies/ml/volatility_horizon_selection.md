## Overview
This module is motivated by a practical issue observed in the baseline strategy.

With a fixed 4-hour horizon (rebalancing every 4 hours), the strategy showed strong gross performance, but became unprofitable after accounting for trading fees.  
Most of the returns were consumed by frequent trading.

Switching to a longer fixed horizon (e.g. 24 hours) reduced trading costs, but also significantly reduced returns.  
The strategy became too slow and failed to capture shorter-term opportunities.

This creates a clear trade-off:
- short horizon → higher raw returns, but excessive fees  
- long horizon → lower fees, but weaker signal  

To address this, we introduce a dynamic horizon based on predicted future volatility.

## Core Idea
The key idea is to adapt the holding period depending on market conditions.

- When volatility is high, the strategy uses shorter horizons to capture fast price movements  
- When volatility is low, it switches to longer horizons to reduce unnecessary trading and avoid fee drag  

Future volatility is estimated using machine learning, and the predicted regime is used to select the horizon.

## Intuition
A fixed horizon is too rigid for crypto markets.

In high-volatility regimes, opportunities are short-lived and require fast reaction.  
In low-volatility regimes, frequent trading leads to overtrading and negative net performance.

A dynamic horizon allows the strategy to:
- capture returns when the market is active  
- reduce turnover when the market is quiet  

## Research Goal
The goal is to test whether a volatility-driven horizon improves net performance by balancing return generation and transaction costs.

This module focuses on whether adapting the trading frequency can preserve profitability that would otherwise be lost to fees.
