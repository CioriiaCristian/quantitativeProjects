# Vanilla Greeks in the Black-Scholes Framework

**Project 2: Analytical & Monte Carlo Estimation of Option Greeks**

This repository implements the full set of **Black-Scholes-Merton (BSM)** Greeks for European vanilla call and put options, with analytical formulas, finite-difference approximations, Monte Carlo-based estimation (pathwise and likelihood ratio methods), and detailed sensitivity investigations.

The focus is on numerical accuracy under different methods.

## Features

- Analytical closed-form formulas for the main Greeks:
  - **Delta** (∂V/∂S) — sensitivity to underlying price
  - **Gamma** (∂²V/∂S²) — convexity / delta sensitivity
  - **Vega** (∂V/∂σ) — sensitivity to volatility (same for call & put)
  - **Theta** (∂V/∂t) — time decay
  - **Rho** (∂V/∂r) — sensitivity to interest rate
- Finite-difference approximations to Greeks (bump-and-revalue method) for validation
- Monte Carlo estimation of Delta using:
  - **Pathwise method** (differentiate payoff along simulated paths)
  - **Likelihood ratio method** (score function / reweighting approach)
- Cross-validation of MC Greeks against analytical values
- Comprehensive sensitivity plots and investigations

## Key Investigations

- **Call Delta vs. Spot Price (S)**:  
  Delta rises from ~0 (deep OTM) to ~1 (deep ITM); smooth S-shaped curve

- **Call Gamma vs. Spot Price (S)**:  
  Gamma peaks near ATM (highest convexity); symmetric around strike

- **Call Vega vs. Volatility (σ), Spot (S), and Time to Maturity (T)**:  
  Vega increases with volatility and time; highest near ATM; decays as T → 0
