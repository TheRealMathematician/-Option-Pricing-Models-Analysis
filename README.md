# -Option-Pricing-Models-Analysis

# README: Option Pricing Models Analysis

## Project Overview
This project analyzes and compares various option pricing models, including the Heston Stochastic Volatility Model and Merton Jump Diffusion Model, for both European and American options. The work demonstrates advanced financial modeling techniques using Monte Carlo simulations and examines option pricing dynamics under different market conditions.

## Key Components

### 1. Model Implementations

**Heston Model (Stochastic Volatility)**
- Applied to ATM European options with different correlation values (-0.30 and -0.70)
- Calculated option prices and Greeks (delta, gamma)
- Verified put-call parity
- Analyzed moneyness effects (0.85-1.10 range)

**Merton Model (Jump Diffusion)**
- Priced European options with varying jump intensities (0.25 and 0.75)
- Computed corresponding Greeks
- Tested put-call parity
- Examined moneyness impact on pricing

**American Options**
- Compared pricing against European equivalents
- Demonstrated early exercise premium

**Exotic Options**
- Priced European Up-and-In (UAI) call options
- Valued European Down-and-In (DAI) put options

### 2. Key Findings

**Pricing Comparisons**
- Heston ATM options:
  - ρ=-0.30: Call=2.87, Put=2.89
  - ρ=-0.70: Call=2.07, Put=3.47
- Merton options:
  - λ=0.75: Call=8.32, Put=7.06
  - λ=0.25: Call=6.80, Put=5.83
- American options showed higher values due to early exercise feature

**Greeks Analysis**
- Heston model showed more sensitive gamma values to correlation changes
- Merton model deltas varied significantly with jump intensity
- Gamma values demonstrated different volatility characteristics between models

**Moneyness Effects**
- Both models showed expected price decay with increasing strike prices
- Merton model produced higher option prices across all moneyness levels
- Heston model showed steeper price decay for out-of-money options

**Exotic Options**
- European UAI call option priced at 0.2998
- European DAI put option priced at 5.3857
- Demonstrated barrier option pricing mechanics

### 3. Technical Implementation

**Methodology**
- Monte Carlo simulations (10,000 paths)
- Stochastic volatility modeling (Heston)
- Jump diffusion processes (Merton)
- Barrier option path-dependent pricing

**Validation**
- Put-call parity verification for both models
- Convergence testing of Monte Carlo results
- Comparative analysis across model types

**Numerical Results**
- Confirmed put-call parity holds for both models
- Demonstrated American option premium over European
- Quantified moneyness effects on option pricing

## Repository Structure

```
/project
│── /notebooks
│   ├── heston_model.ipynb
│   ├── merton_model.ipynb
│   └── american_exotics.ipynb
│── /data
│   ├── parameters.json
│   └── results.csv
│── /docs
│   └── methodology.pdf
├── README.md
└── requirements.txt
```

## Future Work

1. Extend to multi-asset options
2. Implement control variates for variance reduction
3. Add local volatility surfaces
4. Develop real-time pricing dashboard
5. Incorporate machine learning for parameter calibration

This project provides a comprehensive framework for understanding advanced option pricing models and their practical implementation through Monte Carlo methods. The comparative analysis offers insights into model selection for different market conditions and option types.
