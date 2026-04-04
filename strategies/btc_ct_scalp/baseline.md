# Baseline Counter-Trend Strategy

## Overview
This is the core version of the BTC counter-trend scalp framework.

It is built to test whether short-term reversals can be traded systematically when entries are filtered by adaptive trend structure and volatility conditions.

## Core Idea
The strategy looks for local reversals after price moves away from a reference trend line.

The baseline setup uses:
- TRAMA as an adaptive trend filter
- ATR to scale distance and risk thresholds
- short-term execution logic for entry and exit
- fee-aware evaluation

## Signal Logic
The basic trading idea is:

- identify a stretched move away from a local reference
- wait for reversal confirmation
- open a counter-trend position
- manage the trade with stop and target logic

The setup is designed for intraday BTC data and focuses on short holding periods.

## Risk Management
Risk is controlled through:
- ATR-based minimum distance filters
- trailing-stop logic
- predefined take-profit behavior
- explicit treatment of trading costs

## What This Version Tests
This baseline version is meant to answer a simple question:

Can a stripped-down counter-trend setup produce stable behavior before adding more filters and market structure layers?

## Limitations
This version is intentionally simple.  
It does not try to encode every aspect of intraday market behavior and should be treated as a starting point rather than a final trading rule.

## Role in the Project
This file defines the core hypothesis.  
All later additions are extensions of this setup, not separate ideas.
