# Crypto ML Research Framework

## Overview
This folder contains a machine learning research framework for systematic crypto trading.

The project is split into two related but distinct parts.

The first part studies whether future volatility can be predicted well enough to choose a more appropriate trading horizon.  
The second part studies whether machine learning signals can improve cross-sectional portfolio construction by selecting coins for long and short positions and assigning leverage more systematically.

These are not separate trading systems in the narrow sense.  
They are two layers of the same research agenda:
- horizon selection
- cross-sectional asset selection and portfolio scaling

## Structure
- `volatility_horizon_selection.md` — forecasting volatility to choose the trading horizon
- `cross_sectional_selection.md` — selecting long and short coins and assigning leverage

## Research Goals
The main goals of this framework are:
- to test whether machine learning adds value in a realistic trading setting
- to separate signal quality from portfolio construction
- to evaluate out-of-sample stability rather than isolated best-case results
- to understand whether better horizon choice and better cross-sectional ranking can improve risk-adjusted performance

## General Methodology
The framework is built around:
- intraday crypto data
- rolling walk-forward evaluation
- warm-up periods for feature construction
- out-of-sample testing
- comparison against simpler baselines
- performance analysis with return, Sharpe ratio, drawdown, turnover, and benchmark-relative metrics

## Main Themes
- volatility forecasting
- horizon adaptation
- cross-sectional ranking
- long/short portfolio construction
- leverage assignment
- machine learning in financial markets
- robustness and realistic evaluation

## Notes
This project should be read as empirical ML research for crypto markets, not as a finished execution system.

The focus is on what machine learning actually improves, where it fails, and how sensitive the results are to modeling choices.
