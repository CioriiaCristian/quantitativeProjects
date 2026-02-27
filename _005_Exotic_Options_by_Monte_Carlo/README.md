# Exotic Options Pricing via Monte Carlo Simulation

**Project 5: Monte Carlo Pricing of Asian and Continuous Barrier Options**


This project is based on Computer Project 5. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

[Google Colab Link](https://colab.research.google.com/drive/16taZgVhI-stY0GLjDzHGKuSreTg0rYQs)

This repository implements **Monte Carlo** pricing engines for two classic path-dependent exotic options under the Black-Scholes framework.

## Features

- Risk-neutral Monte Carlo path generation (GBM)
- Asian option pricing
- Continuous barrier option pricing:
  - Knock-out (up-and-out, down-and-out)
  - Knock-in (up-and-in, down-and-in)
- Convergence studies across:
  - Monitoring frequency 

## Key Investigations

All results based on Monte Carlo with 10⁵–10⁶ paths per configuration.

- **Convergence rate vs. monitoring frequency**:
  - Asian options: Discrete monthly averaging → significant bias vs. continuous average; convergence improves with more frequent monitoring
  - Barrier options: Discrete monitoring introduces barrier-hitting error (discretization bias)

