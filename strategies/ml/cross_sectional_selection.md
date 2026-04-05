# Cross-Sectional Selection for Long/Short Portfolios

## Overview
This module studies whether machine learning can improve cross-sectional crypto portfolio construction.

The goal is to rank coins, choose candidates for long and short positions, and assign leverage in a more systematic way.

## Core Idea
Rather than trading a single asset in isolation, this framework treats the market as a cross-section.

At each decision point, the model evaluates many coins and estimates which ones are more attractive for long exposure, which ones are weaker and more suitable for short exposure, and how aggressive the position size should be.

## Research Questions
- Can machine learning improve coin selection for long and short portfolios?
- Does cross-sectional ranking remain useful after costs and turnover?
- Can leverage assignment be made more disciplined by linking it to model confidence or expected risk-adjusted payoff?

## Method
The framework typically includes:
- panel data at the coin-time level
- feature construction for each asset
- walk-forward model training
- prediction of return direction, expected return, or related targets
- ranking of assets at each rebalance point
- portfolio construction with long and short baskets
- leverage assignment based on confidence, score strength, or risk rules

## Typical Inputs
This module may use:
- momentum and reversal features
- volatility and ATR-based features
- VWAP and distance measures
- liquidity and turnover measures
- multi-timeframe technical summaries
- market context features
- BTC and market regime variables

## Portfolio Layer
The model output is not treated as a final trade by itself.

It is used to support three portfolio decisions:
- which coins go into the long basket
- which coins go into the short basket
- how much leverage or exposure each position receives

This keeps the research focused on allocation quality rather than raw prediction scores alone.

## Evaluation
The main evaluation questions are:
- whether ranking quality is strong out of sample
- whether long and short baskets remain economically meaningful after costs
- whether leverage rules improve or damage performance
- whether the strategy adds value relative to simpler baselines or equal-weight portfolios

## Main Interpretation
This module is best understood as a portfolio construction and selection framework.

Its value depends not only on predictive power, but also on turnover control, execution realism, and stability across market regimes.

## Role in the Project
This module sits downstream of feature engineering and model training.

It converts model signals into a practical long/short portfolio and studies whether machine learning can improve cross-sectional allocation in a robust way.
