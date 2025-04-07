# Risk Analysis Project

This project was developed as part of the MSc Mathematical Trading and Finance programme at Bayes Business School (formerly Cass). It investigates risk estimation and portfolio construction across a high-volatility asset universe, with a particular focus on Value-at-Risk (VaR), the need for a coherent risk measure like Expected Shortfall, and the impact of distributional assumptions on tail risk metrics.

## Problem

Value-at-Risk is widely taught as a standard measure of portfolio risk. However, applying it in practice reveals deeper modelling choices. Should we use parametric or non-parametric methods? Can we assume normality, or do our data exhibit fat tails? This project explored these questions across three tasks: VaR estimation and backtesting, multi-day loss forecasting, and portfolio risk decomposition for six US tech stocks.

## My Reflections

This project reshaped how I think about risk. We often speak of VaR as a one-size-fits-all measure, but its utility depends heavily on distributional fit. In our case, the dataset consisted of volatile tech stocks that clearly violated Gaussian assumptions. We implemented bootstrapped and parametric VaRs, but their poor backtest results made it obvious that something more robust was needed. I proposed and implemented the filtered block bootstrap to better account for regime shifts and preserve autocorrelation. It worked, and it sparked the idea for my dissertation. On the portfolio side, I gained a much deeper appreciation for how risk-aware portfolio design can differ from naïve equal weighting. Modelling Expected Shortfall also drove home its theoretical superiority to VaR, especially once we saw how distributional failures compound at the tails. Risk isn’t an afterthought; it’s a design constraint.

## Methods

- VaR Estimation: Gaussian, Student’s T, EWMA, Standard Bootstrap, Block Bootstrap, Filtered Block Bootstrap (GARCH)
- Backtesting: Kupiec’s Proportion of Failures (POF), Christoffersen’s Conditional Coverage, KS tests on PIT values
- Loss Forecasting: Gaussian vs empirical comparison for multi-day losses
- Portfolio Optimisation: Risk Parity (parametric and non-parametric), Maximum Diversification, Component VaR

## Repository Structure

```
Risk-Analysis-Project/
├── Images/
├── Results/
├── Task Images/
├── .gitignore
├── Prices.xlsx
├── README.md
├── Report.pdf
├── Task.pdf
├── q1.m
├── q2.m
├── q5.m
```

## Results Summary

| Portfolio Strategy     | Sharpe Ratio | Max Drawdown | VaR Violations (95%) | Final Cumulative Return |
|------------------------|--------------|--------------|-----------------------|--------------------------|
| Equally Weighted       | 1.25         | -0.145       | 7                     | 0.406                    |
| Risk Parity (Param)    | 1.32         | -0.132       | 8                     | 0.425                    |
| Maximum Diversification| 1.30         | -0.138       | 8                     | 0.418                    |
| Risk Parity (Non-Param)| 1.28         | -0.140       | 7                     | 0.412                    |

> Backtesting and PIT analysis highlighted distributional misfit under standard VaR methods, reinforcing the motivation for using Expected Shortfall in high-volatility regimes.

## Requirements

```bash
Requires MATLAB with Statistics and Econometrics Toolboxes.
```

## How to Run

1. Open MATLAB and navigate to the project folder
2. Load `Prices.xlsx` into the workspace
3. Open any question script (e.g. `q1.m`, `q2.m`, `q5.m`) and run sections individually
4. Ensure any saved results are written to `/Images` and `/Results` folders as required

## Further Reading

- Jorion, P.: *Value at Risk: The New Benchmark for Managing Financial Risk*
- Christoffersen, P.: *Elements of Financial Risk Management*

## Authors

- Shaan Ali Remani
- Basil Ibrahim
- Wincy So
- José Santos

---

### Connect

- [LinkedIn](https://www.linkedin.com/in/shaan-ali-remani)  
- [GitHub](https://github.com/RemaniSA)
