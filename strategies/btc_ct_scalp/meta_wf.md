# Meta Walk-Forward Layer

## Overview
This part of the project is not a new trading strategy.

It is a parameter-selection layer built on top of the core BTC counter-trend framework.

The purpose is to decide which parameter sets look more promising out of sample, based on information available before the next evaluation period.

## Core Idea
Instead of choosing one fixed configuration for the whole sample, the framework:
- evaluates many parameter sets on rolling blocks
- extracts summary features from their recent behavior
- ranks or selects candidates for the next period

This makes the setup closer to a realistic research workflow.

## Why This Layer Was Added
The earlier results show that performance is highly sensitive to parameter choice.

That creates a natural research question:

Can parameter instability be handled through a disciplined walk-forward selection process rather than by fixing one "best" setting?

## Method
The meta layer typically includes:
- rolling block evaluation
- feature extraction from recent strategy performance
- top-k candidate selection
- simple machine learning or ranking logic
- next-period out-of-sample testing

## What It Tries to Solve
This layer is meant to reduce:
- dependence on one lucky parameter set
- hindsight bias from full-sample optimization
- instability across market regimes

## Research Value
The main value of this module is methodological.

It helps test whether adaptive parameter selection improves robustness, or whether it simply adds complexity without enough economic benefit.

## Important Point
This should be treated as a research extension, not as proof that dynamic optimization solves the strategy selection problem.

A more complex selection layer can still overfit if it is not evaluated carefully.

## Role in the Project
This module sits above the baseline and extended strategy variants.

It does not generate the original signals.  
It evaluates and selects among parameterized versions of the same framework.
