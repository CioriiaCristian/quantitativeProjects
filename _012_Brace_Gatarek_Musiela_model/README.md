# Brace–Gatarek–Musiela (BGM) / LIBOR Market Model Implementation

**Project 12: Multi-Factor LIBOR Market Model for Caplets and Swaptions**

This project is based on Computer Project 11. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository implements the **Brace–Gatarek–Musiela (BGM)** model — also known as the LIBOR Market Model (LMM) — a lognormal forward-LIBOR framework widely used for consistent pricing of caplets, floors, swaptions, and other interest-rate exotics.

Key aspects covered:

- Simulation of correlated forward LIBOR rates 
- Pricing of **caplets**, **European swaptions** and **Swap Rate Trigger Swap** via Monte Carlo
- Comparison against analytical Black '76 prices (single-factor approximation benchmark)
- Convergence analysis of Monte Carlo estimator
- **Numeraire invariance test** — pricing the same instrument under different measures (terminal vs. spot measure) to validate implementation correctness

## Key Investigations

- **Correlation & volatility structure effects**:
  - Impact of forward rate correlations on swaption skew/smile
  - Sensitivity to volatility term structure (time-dependent or flat)

