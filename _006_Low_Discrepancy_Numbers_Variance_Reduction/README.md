# Low-Discrepancy Sequences for Faster Monte Carlo Convergence

**Project 6: Spectral Decomposition, Cholesky, and Sobol Sequences in Monte Carlo Pricing**

This project is based on Computer Project 6. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository demonstrates the use of **low-discrepancy sequences** (Quasi-Monte Carlo methods) to significantly accelerate convergence in Monte Carlo simulations for option pricing.

The project compares standard pseudo-random Monte Carlo (numpy.random) against quasi-random methods, focusing on:

- Sobol sequences (widely used in finance for their excellent space-filling properties)
- Cholesky decomposition for generating correlated Brownian increments
- Spectral decomposition (PCA-based) as an alternative orthogonalization technique

The goal is to show how these techniques reduce estimator variance and achieve the same accuracy with far fewer paths — a critical skill in production pricing and risk engines.

## Features

- Generation of Sobol low-discrepancy sequences (via scipy.stats.qmc.Sobol)
- Transformation from unit hypercube → correlated Gaussian increments using:
  - Cholesky decomposition of the covariance matrix
- Construction of Geometric Brownian Motion paths using low-discrepancy drivers
- Pricing of vanilla European calls/puts and simple exotics (e.g., Asian) as test cases
- Visualization of convergence curves and error decay rates

## Key Investigations

- **Convergence speedup**:
  - Sobol sequences typically achieve **O(1/N)** error decay (vs. **O(1/√N)** for pseudo-random MC)
  - In practice: 5–50× fewer paths needed to reach the same standard error, depending on dimension and payoff smoothness

