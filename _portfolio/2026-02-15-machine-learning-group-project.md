---
title: "Detecting MEV Bot Addresses on Ethereum"
collection: portfolio
section: fintech_grad
permalink: /portfolio/mev-bot-detection/
date: 2026-04-15
project_period: "Jan 2026 - Apr 2026"
header:
  teaser: projects/mev-bot-detection.svg
excerpt: "Supervised classification of MEV bot addresses on Ethereum via on-chain behavioral feature engineering; resolved internal vs. external validity gap using weak-positive label augmentation."
---

Group ML project detecting Maximal Extractable Value (MEV) bots on Ethereum mainnet using supervised classification of address-level behavioral features.

## Data & Feature Engineering

- Processed 33.5 hours of Ethereum mainnet data (1.50M transactions, 3.65M token transfers) across 481,964 unique addresses.
- Engineered 19 behavioral features capturing activity volume, execution pattern, and transfer composition; confirmed discriminability via Mann-Whitney U tests and Cliff's delta.

## Modeling & Evaluation

- Trained Logistic Regression, Random Forest, and XGBoost under 121:1 class imbalance; applied **weak-positive label augmentation** using ZeroMEV data to expand the positive class and improve generalizability.
- Discovered the **baseline trap**: without augmentation, models achieved near-perfect internal AUC (0.999) yet scored 0/10 on every external validation metric — learning label artifacts rather than true MEV behavior.
- Final XGBoost model achieved OOF AUC = 0.9833, Precision@100 = 0.99, and identified 6/10 top sandwich-attack extractors on external holdout validation.

Links:
- [Code (GitLab)](https://gitlab.oit.duke.edu/yt234/ml540)
