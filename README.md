# ETF Machine Learning Signal Pipeline

## Overview
This project implements a **production-ready machine learning pipeline** for forecasting short-term ETF return directions and converting model outputs into actionable trading signals.

Rather than predicting exact prices, the system focuses on **probabilistic classification** (up/down movement), following industry best practices for time-series modeling, evaluation, and deployment.

The project is designed to demonstrate:
- Proper handling of time-series data
- Leakage-free feature engineering
- Walk-forward validation
- Reproducible ML pipelines
- Decision-oriented evaluation beyond raw model accuracy

---

## Problem Statement
Financial time-series modeling is particularly prone to common ML pitfalls such as:
- Data leakage
- Overfitting
- Unrealistic evaluation procedures

The goal of this project is to answer the following question:

> Can historical market data be used to generate **robust and reproducible predictive signals** when evaluated under realistic, production-like conditions?

---

## Project Scope
- **Assets**: Liquid ETFs (e.g., SPY, QQQ, IWM)
- **Prediction Task**: Binary classification (positive vs negative future return)
- **Model Outputs**: Probabilities used to generate trading signals
- **Evaluation**: ML metrics + trading-oriented performance metrics

This is **not** a high-frequency trading system nor a claim of guaranteed profitability.

---

## Data
- Historical price and volume data
- Adjusted close prices to account for splits and dividends
- Data is downloaded programmatically and **not versioned** in this repository

Directory structure:
```text
data/
├─ raw/        # downloaded data (ignored by git)
├─ interim/    # intermediate transformations
└─ processed/  # final datasets for modeling

