# TRAMA-Based Strategy

## Overview
This is a TRAMA-based strategy applied to intraday BTC data.  
It combines adaptive moving averages, multi-timeframe structure, and simple execution rules to study market behavior.

## What is TRAMA
TRAMA (Trend Regularity Adaptive Moving Average) is an adaptive moving average.  
It adjusts its smoothing based on how consistent the trend is: smoother in noise, more reactive in strong trends.

## Core Idea
The strategy uses:
- a fast TRAMA on 5-minute data  
- a slow TRAMA on 60-minute data  

Signals come from how price interacts with the fast TRAMA, filtered by the higher-timeframe trend.

## Entry Logic
There are three types of entries:
- Counter-trend: after a cross of the fast TRAMA with sufficient distance from the slow TRAMA  
- Trend-following: after a retest of the slow TRAMA with confirmation  
- Flip: after failed counter-trend moves  

## Risk Management
- ATR-based distance filters  
- Partial take-profit  
- Different trailing stops for counter-trend and trend trades  
- Symmetric logic for long and short  

## Research Objective
The goal is not to find the best single run, but to understand how stable this setup is across parameter choices.

## Main Finding
Monte Carlo tests show a wide spread of outcomes.  
Performance varies a lot depending on parameters, so the key question here is robustness, not peak returns.
