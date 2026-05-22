# Portfolio Optimisation

Tax-aware portfolio rebalancing with personalised risk profiles, built in Python.

## Overview

This project explores a systematic approach to portfolio management that goes beyond naive rebalancing. It combines:

- **Tax-aware rebalancing** — accounts for capital gains tax implications when deciding whether to sell positions
- **Personalised risk profiles** — adapts allocation targets based on user-defined risk tolerance
- **Optimisation framework** — finds rebalancing trades that minimise tax drag while maintaining target allocations

## Contents

| File | Description |
|------|-------------|
| `portfolioOptimisation.ipynb` | Main notebook: data loading, optimisation logic, results |
| `portfolio optimisation approach.pdf` | Write-up of the methodology and design choices |

## Approach

The core idea is to treat rebalancing as a constrained optimisation problem:

- **Objective**: minimise deviation from target weights + tax cost of trades
- **Constraints**: no short-selling, stay within user risk band
- **Risk profiles**: conservative / balanced / aggressive, with different target allocations

## Setup

```bash
pip install numpy pandas scipy matplotlib
jupyter notebook portfolioOptimisation.ipynb
```

## Key Results

- Demonstrates that naive rebalancing can trigger unnecessary taxable events
- Tax-aware approach reduces realised gains while maintaining portfolio alignment
- Risk profile personalisation shifts equity/bond/cash split significantly across profiles
