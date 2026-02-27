# Rough Volatility Models – Rough Heston Implementation

**Monte Carlo Pricing and Validation of the Rough Heston Model**

This repository implements the **Rough Heston stochastic volatility model** — a fractional extension of the classical Heston model where volatility follows a **fractional Brownian motion** with Hurst parameter H < 0.5 (typically H ≈ 0.1), producing realistic short-term volatility-of-volatility and power-law autocorrelation observed in empirical data.

The implementation focuses on:

- Euler discretization of the rough variance process
- Analytical sanity checks using the known characteristic function and exact variance expectation formulas
- Monte Carlo pricing of vanilla and exotic options
- Generation of the **at-the-money (ATM) forward skew** and comparison to market-observed empirical skew

This work was part of my MSc thesis ("A Monte Carlo approach to fractional Brownian motion", University of Bologna, 2023), evaluating the practical usability of Euler schemes in rough volatility contexts.

## Features

- Simulation of Rough Heston dynamics via Euler discretization of the fractional variance process
- Analytical sanity checks:
  - Exact expectation of integrated variance E[∫ v_t dt]
- Monte Carlo pricing engines:
  - European vanilla calls/puts
  - Asian options
- ATM forward skew computation: ∂σ_imp / ∂k |_{k=0} as function of maturity
