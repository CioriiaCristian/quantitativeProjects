# Multi-Asset Options Pricing: Quantos & Margrabe Exchange Options

**Project 8: Analytical & Monte Carlo Pricing of Quanto and Margrabe Options**

This project is based on Computer Project 8. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository implements pricing for two classic **multi-asset** / **cross-currency** exotic options:

- **Quanto options** — options on a foreign asset with payoff denominated in domestic currency (fixed exchange rate at maturity)
- **Margrabe exchange options** — options to exchange one risky asset for another (no fixed strike, pure relative value)

Both are priced using:

1. Closed-form **analytical formulas** (Black-Scholes style generalizations)
2. **Monte Carlo simulation** under correlated Geometric Brownian Motions

The project focuses on cross-validating the two methods and studying the **convergence behavior** of the Monte Carlo estimator (variance, standard error, number of paths required).

## Features

- Analytical pricing:
  - Quanto call/put (fixed FX rate, dividend & correlation adjustments)
  - Margrabe exchange option (Margrabe 1978 formula)
- Monte Carlo pricing:
  - Correlated GBM paths using Cholesky decomposition
  - Risk-neutral simulation for both assets
  - Payoff evaluation in domestic currency (quanto) or asset units (Margrabe)
- Convergence analysis:
  - Standard error vs. number of paths
  - Comparison of MC price & confidence interval to analytical truth

