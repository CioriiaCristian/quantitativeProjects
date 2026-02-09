# Vanilla Options Pricing in the Black-Scholes Framework

**Project 1: Analytical & Monte Carlo Implementation of European Vanilla Options**

This project is based on Computer Project 1. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

[Google Colab Link](https://colab.research.google.com/drive/1wUV6PArEeqXT3etI47sMv3KYElvfj3PS#scrollTo=fCO8Tqyk2_of)

This repository contains a complete Python implementation of the **Black-Scholes-Merton (BSM)** model for pricing European vanilla call and put options, along with rigorous consistency checks, Monte Carlo validation, and sensitivity investigations.

The goal was to build a numerically stable, well-tested pricing engine from first principles, verify model properties via no-arbitrage bounds and parity, and explore volatility dependences.

## Features

- Analytical closed-form pricing (Black-Scholes formula) for calls and puts
- Comprehensive **consistency & no-arbitrage checks**
- Monte Carlo simulation of **Geometric Brownian Motion** (GBM) paths
  - One-step simulation
  - Multi-step Euler discretization
- Cross-validation of MC prices against analytical BSM prices
- Convergence analysis (Variance vs. number of paths / time steps)
- Volatility sensitivity studies (call/digital call prices, ATM behavior)

## Consistency & No-Arbitrage Checks

The implementation includes the following analytical verifications (all pass within numerical tolerance):

- **Put-Call Parity**:  
- **Monotonicity w.r.t. Strike**:  
  Call price decreases monotonically as strike K increases  

- **Lower & Upper Bounds for Calls**:  
  All prices lie strictly within bounds

- **Convexity of Call Price w.r.t. Strike**:  
  Second derivative w.r.t. K is positive → price is convex (verified numerically)

- **Call Spread vs. Digital Call Approximation**:  
  Bull call spread (C(K₁) - C(K₂)) approximates a digital (binary) call paying 
  Checked convergence as spread width → 0

## Monte Carlo Validation

- Simulated underlying asset paths under the risk-neutral measure using **Geometric Brownian Motion**:
  - One-step simulation: 
  - Multi-step Euler discretization for path-dependent checks
- Priced vanilla calls/puts by averaging discounted payoffs
- Compared MC estimates to analytical BSM prices
- Studied **convergence behavior**:
  - RMSE decreases as ~1/√N (N = number of paths)
  
## Key Investigations

- **Option Price Behavior vs. Volatility (σ)**:  
  - Call and put prices increase with volatility (positive vega)  

- **At-the-Money (ATM) Behavior**:  
  - ATM call/put prices with respect to volatility
