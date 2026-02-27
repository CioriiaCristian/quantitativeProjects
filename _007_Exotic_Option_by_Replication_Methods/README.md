# Replication Portfolio Pricing for Continuous Barrier Options

**Project 7: Static Replication of Continuous Barrier Options & Convergence Analysis**

This project is based on Computer Project 7. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository implements **static replication portfolios** to price continuous barrier options (up-and-out / down-and-out calls and puts) under the Black-Scholes framework.

Instead of dynamic delta-hedging or path-dependent Monte Carlo, the method constructs a static portfolio of vanilla options that replicates the barrier payoff exactly in the continuous limit.

The project studies numerical convergence of the replication approximation and extends the framework to **time-dependent volatility** regimes.

## Features

- Static replication of continuous up-and-out and down-and-out barrier options using a continuum (discretized) of vanilla calls/puts
- Discretization of the replication integral with user-controlled number of strikes / time steps
- Analytical Black-Scholes prices for the constituent vanilla options
- Convergence analysis of replication error vs.:
  - Number of strikes in the portfolio (discretization fineness)
  - Number of time steps in volatility discretization (when σ(t) varies)
- Support for time-dependent volatility σ(t):
  - Deterministic functions (linear, exponential decay, step functions, etc.)
  - Effective forward volatility integration for replication weights
- Pricing under constant and time-varying volatility configurations
- Error metrics: absolute/relative difference vs. closed-form continuous barrier prices (when available) or high-fidelity Monte Carlo reference

## Key Investigations

- **Convergence vs. discretization size**:
  - Replication error decreases rapidly with increasing number of strikes (typically O(1/N) or better)

- **Numerical stability & efficiency**:
  - Trade-off between number of vanilla options (strikes) and pricing accuracy
  - Comparison to full path-dependent Monte Carlo in terms of speed and variance (replication is deterministic once discretized)
