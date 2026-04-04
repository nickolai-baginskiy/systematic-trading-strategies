# Extended Framework: Momentum, VWAP, and Zones

## Overview
This version extends the baseline counter-trend setup by adding more market context.

The goal is to avoid taking every reversal signal and instead focus on situations where price behavior, momentum, and intraday structure support the trade.

## Main Additions

### Momentum Filter
Momentum is used to distinguish between weak exhaustion moves and strong directional pressure.

This helps answer a practical question:
is the market slowing down into a reversal, or is it still moving with enough force to invalidate a counter-trend entry?

### VWAP Context
VWAP is used as an intraday anchor.

It adds information about where price stands relative to the session's average traded level and helps separate stretched moves from more neutral conditions.

### Zones and Local Structure
This layer adds local price structure, including ideas such as:
- supply and demand zones
- density areas
- local pivots

These filters are used to improve entry quality and trade management rather than to replace the main strategy logic.

## Why These Filters Matter
The baseline setup can generate too many signals in noisy conditions.  
The extended version asks whether additional context can improve:
- selectivity
- trade quality
- post-cost performance
- robustness across parameter choices

## Research Focus
This version is not just about improving return.

It is mainly used to test whether richer market context reduces false positives and makes the strategy less fragile under repeated evaluation.

## Practical Interpretation
The extended framework treats counter-trend entries as valid only when:
- price is sufficiently stretched
- momentum is consistent with exhaustion or reversal
- intraday context is not hostile
- local structure gives a reasonable area for execution

## Role in the Project
This is the main research version of the strategy.

It keeps the original counter-trend idea but adds the filters needed for more realistic testing.
