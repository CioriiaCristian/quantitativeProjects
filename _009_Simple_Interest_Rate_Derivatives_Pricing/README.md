# Simple Interest-Rate Derivative Pricing

**Project 9: Analytical Pricing of FRAs, Caps/Floors, and Swaptions **

This project is based on Computer Project 9. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

This repository implements closed-form analytical pricing for key interest-rate derivatives using the (lognormal forward rate) model — the market standard for pricing caplets, floors, FRAs, and European swaptions under the assumption of lognormal forward rates or swap rates.

The project covers:

- Forward Rate Agreements (FRAs)
- Caplets and floorlets
- European swaptions (payer and receiver)

All implementations use exact formulas with proper day-count conventions, discounting, and annuity adjustments for swaptions.

## Features

- Analytical pricing functions for:
  - **Forward Rate Agreements** (FRA): settlement at start or end of period
  - **Caplets** / **Floorlets**: single-period cap/floor components
  - **European Swaptions**: payer (right to pay fixed) and receiver (right to receive fixed)
