# Hedging Strategies in a Black-Scholes World

**Project 3: Hedging in a Black Scholes World**


This project is based on Computer Project 3. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository implements and compares hedging strategies for European vanilla options under the **Black-Scholes-Merton (BSM)** framework using Monte Carlo simulations. The core focus is quantifying **hedging P&L variance** (terminal error) in discrete-time rebalancing scenarios, analyzing sensitivity to time step size (Δt), drift (μ), volatility (σ), and extensions to time-dependent volatility σ(t).

Tasks performed:
- Comparison of Delta hedging, Stop-Loss, and Gamma hedging
- Variance dependence vs key parameters
- Practical evaluation of hedging with time-varying volatility using instantaneous, RMS, and forward RMS approaches

## Features

- Monte Carlo path generation via Geometric Brownian Motion (GBM)
- Discrete-time rebalancing at user-defined intervals (Δt)
- Hedging strategies:
  - **Delta Hedging** — dynamic adjustment to neutralize Delta
  - **Stop-Loss Strategy** — buy/sell underlying based on moneyness thresholds
  - **Gamma Hedging** — second-order correction (via additional instruments or approximation)
- Computation of terminal P&L distribution and variance
- Time-dependent volatility extensions:
  - Instantaneous σ(t) for local Delta
  - Root-Mean-Square (RMS) volatility over [0,T]
  - Forward RMS volatility from current time to maturity
- Parameter sweeps and visualization of variance vs. Δt, μ, σ

### Delta Hedging
- Portfolio variance decreases with smaller time step size (Δt), converging to near-zero in continuous limit
- Portfolio variance increases strongly with volatility (σ)

### Stop-Loss Strategy
- Higher variance than Delta hedging for same Δt
- More pronounced increase with σ; sensitive to μ in directional bias

### Gamma Hedging
- Reduced variance compared to pure Delta hedging, especially for larger Δt
- Faster convergence to low error with frequent rebalancing

### Time-Dependent Volatility
- Simulated σ(t) profiles (e.g. time-varying)
- **Instantaneous volatility hedging**: Positive bias to Portfolio Value, Variance does not converge to 0
- **RMS volatility over whole horizon**:Negative bias to Portfolio Value, Variance does not converge to 0
- **Forward RMS volatility**: No bias present, variance convergences to 0 for Δt-> 0
