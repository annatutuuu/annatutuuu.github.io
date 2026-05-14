---
title: "Volatility Forecasting & Risk Estimation — QQQ"
collection: portfolio
section: fintech_grad
permalink: /portfolio/volatility-forecasting-qqq/
date: 2026-04-15
project_period: "Jan 2026 - Apr 2026"
header:
  teaser: "projects/One-step-ahead volatility forecast.png"
excerpt: "Compared EWMA, GARCH, and GJR-GARCH models for one-step-ahead volatility forecasting on QQQ; evaluated VaR/ES calibration and volatility-targeting strategy performance."
---

Empirical study comparing conditional volatility models for market risk forecasting on QQQ (Nasdaq-100 ETF), using 26 years of daily return data (2000–2026).

## Volatility Modeling

- Implemented and compared three conditional volatility models — **EWMA, GARCH(1,1), and GJR-GARCH(1,1)** — to forecast one-step-ahead conditional variance on QQQ daily returns.
- Documented stylized facts motivating time-varying volatility models: volatility clustering, fat tails (kurtosis = 7.58), and asymmetric shock responses (leverage effect).
- Estimated GJR-GARCH asymmetry parameter γ ≈ 0.147 (p < 0.001), confirming statistically significant leverage effects in QQQ returns.

## Out-of-Sample Forecasting

- Applied an **expanding window** estimation scheme over a 1,323-observation out-of-sample period (2021–2026), re-estimating GARCH parameters at each step to avoid look-ahead bias.
- Evaluated forecast accuracy using MSE and MAE against squared-return realized volatility proxies; GJR-GARCH outperformed both EWMA and GARCH across all loss metrics, reducing volatility MSE by ~8% relative to EWMA.

## Risk Management Applications

- Derived **VaR and Expected Shortfall** estimates from model-implied volatility forecasts under conditional normality; backtested at 95% and 99% confidence levels.
- GJR-GARCH achieved the lowest 95% VaR exceedance rate (5.74% vs. 5% target), outperforming EWMA (6.88%) and GARCH (6.20%); all models underestimated extreme tail risk at 99%, suggesting heavier-tailed innovations as a future extension.
- Evaluated a **volatility-targeting strategy** across models; GJR-GARCH delivered the highest Sharpe-like ratio (0.052) while maintaining realized volatility close to the 1% target.
