# Quant Project – Randomness in FX vs Coin Flips

**Goal:** Tests whether EUR/USD daily returns behave like a random walk (fair coin) using statistical tests and simulations.

## Data
- **Asset:** EUR/USD exchange rate (Yahoo Finance ticker: `EURUSD=X`)
- **Frequency:** Daily closing prices
- **Period:** January 2010 – January 2025 (~3,900 observations)
- **Transformations:**
  - Returns calculated as daily percentage changes
  - Converted to binary sequence: 1 = up day, 0 = down day

This preprocessing allows direct comparison with simulated coin flips.

## Methods
- Bias test (binomial)
- Runs test (Wald-Wolfowitz)
- Longest streak Monte Carlo
- Markov transition probabilities
- Autocorrelation & Ljung-Box
- Hurst exponent (R/S method)
- Shannon entropy
- Permutation test (toy momentum rule)

## Key Results
- No directional bias (49.5% up days, p=0.52)
- Runs and longest streaks consistent with randomness
- No short-term memory (Markov, permutation)
- Volatility clustering in squared returns (p < 1e-70)
- Mild persistence (Hurst ≈ 0.55)
- Entropy ≈ 1.0 bits → near-max unpredictability

## Deliverables
- 📑 [Research Paper PDF](docs/Are Markets Random_ EUR_USD vs Coin Flips.pdf)
- 📸 Figures in `docs/charts/`
- 📂 [Notebook](notebooks/fx_vs_coin_randomness.ipynb)
