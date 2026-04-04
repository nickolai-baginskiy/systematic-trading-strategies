# BTC Counter-Trend Scalp Framework

## Overview
This folder contains a family of intraday BTC trading frameworks built around short-term counter-trend logic.

The main idea is to study whether local price dislocations can be traded in a systematic way when signals are filtered by adaptive trend structure, volatility conditions, intraday anchors, and execution rules.

This is not a collection of unrelated strategies.  
It is one research line with several layers:
- a baseline counter-trend setup
- an extended version with momentum, VWAP, and zone filters
- a meta walk-forward layer for parameter selection

## Structure
- `baseline.md` — core counter-trend setup
- `momentum_vwap_zones.md` — extended signal filters and market structure context
- `meta_wf.md` — walk-forward parameter selection and meta-model layer

## Research Goal
The goal is not to optimize a single backtest, but to understand:
- whether the setup has economic value after costs
- how sensitive performance is to parameters
- which filters improve stability
- whether parameter selection can be made more robust over time

## Main Themes
- intraday BTC trading
- counter-trend execution
- adaptive indicators
- fee-aware backtesting
- parameter sensitivity
- robustness testing
- walk-forward model selection

## Notes
This framework is best viewed as empirical strategy research rather than a finished production system.
