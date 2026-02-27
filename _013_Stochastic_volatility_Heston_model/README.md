# Heston Stochastic Volatility Model

**Project 13: Monte Carlo Pricing of Exotic Options under Heston Dynamics**

This repository implements the **Heston stochastic volatility model** (1993) — one of the most widely used frameworks for capturing volatility smiles and skews observed in real markets.

The implementation is based on the moment-matching Quadratic Exponential scheme of Leif Andersen.

Key elements:

- Full Heston dynamics simulation (CIR process for variance, correlated Brownian motions for asset and volatility)
- Monte Carlo pricing of vanilla and exotic options under Heston
- Analysis of implied volatility surfaces and smile/skew generation

The project demonstrates the limitations of constant-volatility models and the importance of stochastic volatility for realistic derivatives pricing.

## Features

- Monte Carlo pricing engines for:
  - European vanilla calls/puts
  - Asian options
- Analytical benchmark using the Expectation and Variance of the volatility process 
- Implied volatility extraction from Heston prices (via root-finding on BS formula)
