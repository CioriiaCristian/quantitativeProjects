# Recombining Trees for Option Pricing

**Project 4: Binomial & Trinomial Lattice Methods for Vanilla, American, and Barrier Options**


This project is based on Computer Project 4. of the book The Concepts and Practice of Mathematical Finance by Mark S. Joshi, Second Edition (2008)

[Google Colab Link](https://colab.research.google.com/drive/1gHmyh404eCYCSargWSE4MEPfne2-HBNE#scrollTo=Y_7nLnIMB_hL)

This repository implements **binomial** and **trinomial** tree models for pricing European and American options, with extensions to barrier options. The focus is on numerical convergence to the Black-Scholes-Merton (BSM) analytical prices.

## Features

- **Binomial tree** 
- **Trinomial tree**
- Recombining lattice construction in log-price space
- Pricing of:
  - European vanilla call/put
  - American vanilla put 
  - Continuous barrier options 

- Convergence analysis vs. number of time steps (comparison to BSM closed-form)

## Key Investigations & Results

- **Convergence to Black-Scholes**:
  - Binomial trees show oscillatory convergence (typical sawtooth pattern due to node alignment with strike)
  - Trinomial trees generally offer smoother and faster convergence (especially with fewer steps), better matching higher moments of the lognormal distribution

- **American Options**:
  - Early-exercise boundary captured via max(intrinsic, European) at each node

- **Barrier Options**:
  - Continuous monitoring approximated by checking barrier condition at each node

- **Binomial vs. Trinomial Comparison**:
  - Trinomial often requires fewer steps for similar accuracy (especially near barriers or for American features)
  - Trade-off: slightly higher per-step computation but overall efficiency gain

All pricing validated against analytical BSM prices for European vanillas.
