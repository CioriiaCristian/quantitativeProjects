# Vanilla Options Pricing in the Black-Scholes Framework

**Project 1: Analytical & Monte Carlo Implementation of European Vanilla Options**

This repository contains a complete Python implementation of the **Black-Scholes-Merton (BSM)** model for pricing European vanilla call and put options, along with rigorous consistency checks, Monte Carlo validation, and sensitivity investigations.

The goal was to build a numerically stable, well-tested pricing engine from first principles, verify model properties via no-arbitrage bounds and parity, and explore key behaviors (especially volatility dependence).

## Features

- Analytical closed-form pricing (Black-Scholes formula) for calls and puts
- Computation of option **Greeks** (Delta, Gamma, Vega, Theta, Rho)
- Comprehensive **consistency & no-arbitrage checks**
- Monte Carlo simulation of **Geometric Brownian Motion** (GBM) paths
  - One-step exact simulation
  - Multi-step Euler discretization
- Cross-validation of MC prices against analytical BSM prices
- Convergence analysis (error vs. number of paths / time steps)
- Volatility sensitivity studies (call/digital call prices, ATM behavior)

## Consistency & No-Arbitrage Checks

The implementation includes the following analytical verifications (all pass within numerical tolerance):

- **Put-Call Parity**:  
  `C - P = S - K e^{-rT}` → verified for a wide range of parameters

- **Monotonicity w.r.t. Strike**:  
  Call price decreases monotonically as strike K increases  
  Put price increases monotonically as strike K increases

- **Lower & Upper Bounds for Calls**:  
  - Lower: max(S - K e^{-rT}, 0)  
  - Upper: S  
  All prices lie strictly within bounds

- **Convexity of Call Price w.r.t. Strike**:  
  Second derivative w.r.t. K is positive → price is convex (verified numerically)

- **Call Spread vs. Digital Call Approximation**:  
  Bull call spread (C(K₁) - C(K₂)) approximates a digital (binary) call paying 1 if S_T > K  
  Checked convergence as spread width → 0

## Monte Carlo Validation

- Simulated underlying asset paths under the risk-neutral measure using **Geometric Brownian Motion**:
  - Exact one-step simulation: `S_T = S_0 * exp((r - σ²/2)T + σ √T Z)`, Z ~ N(0,1)
  - Multi-step Euler-Maruyama discretization for path-dependent checks
- Priced vanilla calls/puts by averaging discounted payoffs
- Compared MC estimates to analytical BSM prices
- Studied **convergence behavior**:
  - RMSE decreases as ~1/√N (N = number of paths)
  - Variance reduction techniques considered for future extensions

## Key Investigations

- **Option Price Behavior vs. Volatility (σ)**:  
  - Call and put prices increase with volatility (positive vega)  
  - Plotted price surfaces and slices

- **At-the-Money (ATM) Behavior**:  
  - ATM call/put prices ≈ (S σ √T)/√(2π) for small T (linear in volatility)  
  - Digital call probability (N(d₂)) behavior near ATM
