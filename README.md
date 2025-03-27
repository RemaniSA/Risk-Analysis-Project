# Risk Analysis Project (2024/25)

This project was developed as part of the MSc Mathematical Trading and Finance programme at Bayes Business School (formerly Cass). It explores risk estimation techniques across multiple levels of market and portfolio analysis using MATLAB. The project investigates Value-at-Risk (VaR) methodologies, backtesting procedures, and portfolio risk decomposition across both parametric and non-parametric frameworks.

## Overview

The analysis is conducted using daily adjusted closing prices of six large-cap technology stocks from 2014 to 2024. The project is structured around three key tasks:

1. **VaR Estimation and Backtesting** – Rolling-window VaR forecasts at 90% and 99% confidence using six methods: 
   - Standard Bootstrap
   - Block Bootstrap
   - Filtered Block Bootstrap (GARCH)
   - Gaussian
   - Student's T (via Method of Moments)
   - EWMA (RiskMetrics)

2. **Multi-Day Loss Estimation** – Comparison of empirical (bootstrapped) and Gaussian estimates for cumulative loss probabilities over a 50-day horizon.

3. **Portfolio Risk Decomposition** – Out-of-sample comparison of four strategies:
   - Equally Weighted
   - Risk Parity (Parametric)
   - Maximum Diversification
   - Risk Parity (Non-Parametric)

## Repository Structure

```
Risk-Analysis-Project/
├── Images/                         # Visual outputs from VaR and portfolio analyses
├── Results/                        # Saved tables and backtesting outputs
├── Prices.xlsx                     # Daily asset prices (6 tech stocks)
├── Report.pdf                      # Final write-up with results and interpretation
├── Task.pdf                        # Coursework brief
├── Codes                           # MATLAB scripts for each task
└── README.md
```

## Results Summary

| Portfolio Strategy     | Sharpe Ratio | Max Drawdown | VaR Violations (95%) | Final Cumulative Return |
|------------------------|--------------|--------------|-----------------------|--------------------------|
| Equally Weighted       | 1.25         | -0.145       | 7                     | 0.406                    |
| Risk Parity (Param)    | 1.32         | -0.132       | 8                     | 0.425                    |
| Maximum Diversification| 1.30         | -0.138       | 8                     | 0.418                    |
| Risk Parity (Non-Param)| 1.28         | -0.140       | 7                     | 0.412                    |

> Backtesting and probability integral transform (PIT) analysis were applied to assess model calibration and distributional accuracy.

## How to Run

All code is implemented in MATLAB. To execute:

1. Ensure the dataset (`Prices.xlsx`) is in the working directory.
2. Open `script.m` (for the script of interest).
3. Set `figswitch = 1` and `resultswitch = 1` to save outputs to `/Images/` and `/Results/`.

## Methods

- **VaR Estimation**: Gaussian, T-distribution, EWMA, GARCH-filtered Bootstrap, Block Bootstrap, Non-parametric
- **Backtesting**: Kupiec’s POF, Christoffersen’s Conditional Coverage, KS tests on PIT
- **Portfolio Optimisation**: Risk Parity (param/np), Maximum Diversification, Component VaR decomposition

## Authors

- Shaan Ali Remani  
- Basil Ibrahim  
- José Santos  
- Wincy So

# Coursework Brief

![Risk Analysis Page 1](https://github.com/RemaniSA/Risk-Analysis-Project/blob/main/Task%20Images/RACW_p1.jpg)

![Risk Analysis Page 2](https://github.com/RemaniSA/Risk-Analysis-Project/blob/main/Task%20Images/RACW_p2.jpg)

![Risk Analysis Page 3](https://github.com/RemaniSA/Risk-Analysis-Project/blob/main/Task%20Images/RACW_p3.jpg)

![Risk Analysis Page 4](https://github.com/RemaniSA/Risk-Analysis-Project/blob/main/Task%20Images/RACW_p4.jpg)

![Risk Analysis Page 5](https://github.com/RemaniSA/Risk-Analysis-Project/blob/main/Task%20Images/RACW_p5.jpg)
