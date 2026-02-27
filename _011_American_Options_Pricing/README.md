# American Options Pricing: Portfolio Replication & Binomial Tree Methods

**Project 11: Numerical Pricing of American Options with Early-Exercise Feature**

This repository implements two distinct approaches for pricing **American-style options** (which allow early exercise), where the standard Black-Scholes closed-form solution no longer applies due to the optimal exercise boundary.

Methods implemented:

1. **Portfolio replication / static replication** — constructing a portfolio of European options that approximates the American payoff 

2. **Recombining binomial tree** — discrete-time lattice method with backward induction and explicit early-exercise check at each node

The project focuses on numerical accuracy, comparison of the two methods, and convergence behavior as the number of time steps (or replication points) increases.

## Features

- **Binomial tree implementation**:
  - Recombining lattice in log-price space
  - Backward induction with early-exercise decision: max(intrinsic value, continuation value)
  - Pricing of American put options
- **Portfolio replication approach**:
  - Discretized static portfolio of European calls/puts to replicate the early-exercise premium
  - Approximation of the optimal exercise boundary via strike grid

