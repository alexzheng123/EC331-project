# 📈 Market Efficiency of Bitcoin in 2024

This repository contains the full code for my undergraduate dissertation:  
**"Market Efficiency of Bitcoin in 2024: Evidence from Statistical and Deep Learning Models"**,  
submitted for EC331: Research in Applied Economics at the University of Warwick.

📄 [Full Dissertation (PDF)](./EC331__Research_in_Applied_Economics.pdf)

---

## Overview

This study investigates the **weak form Efficient Market Hypothesis (EMH)** in the Bitcoin market by analysing **1-minute BTC/USD data from 2024**. I apply both **traditional statistical tests** and **deep learning models**, including a novel **VMD-GRU-Attention** architecture.

Despite extensive volatility in Bitcoin prices, I find evidence of **predictable patterns**, especially when using the VMD-GRU-Attention model, challenging the weak form EMH.

---
## Sample Visualisations

### Bitcoin Price & Volume (2024)

<img src="https://raw.githubusercontent.com/alexzheng123/EC331-project/main/EMH/images/No%20titles/Bitcoin%20Close%20Price%20and%20volume.png" width="600"/>

---

### VMD-GRU-Attention Model Architecture

<img src="https://raw.githubusercontent.com/alexzheng123/EC331-project/main/EMH/images/No%20titles/VMD-GRU-Attention-steps.png" width="600"/>

---

### VMD Decomposition of Returns

<img src="https://raw.githubusercontent.com/alexzheng123/EC331-project/main/EMH/images/No%20titles/VMD%20decomposition.png" width="600"/>

---

### Forecast vs Actual (Validation & Test)

<div style="display: flex; gap: 10px;">
  <img src="https://raw.githubusercontent.com/alexzheng123/EC331-project/main/EMH/images/No%20titles/VMD-GRU-Att%20Forecast%20vs%20Actual%20Returns%20(Validation%20Set).png" width="48%"/>
  <img src="https://raw.githubusercontent.com/alexzheng123/EC331-project/main/EMH/images/No%20titles/VMD-GRU-Att%20Forecast%20vs%20Actual%20Returns%20(Test%20Set).png" width="48%"/>
</div>

---

## Research Questions

- Does the Bitcoin market in 2024 exhibit weak form efficiency?
- Can deep learning models forecast high-frequency Bitcoin returns more accurately than traditional econometric models?

---

## Repository Structure

This repo includes all code used in the dissertation:

### Statistical Testing
- `Statistical_tests.ipynb` – Ljung-Box, Runs test, Variance Ratio, Hurst exponent, BDS test

### Econometric & Deep Learning Models
- `ARIMA.ipynb` – ARIMA(1,0,2) model
- `GRU_1.ipynb` – GRU model using only price and technical indicators
- `GRU_2.ipynb` – GRU model including macroeconomic and sentiment data
- `VMD_AttGRU.ipynb` – Attention before GRU (from literature)
- `VMD_GRU_Attention.ipynb` – Proposed model: GRU before Attention
- `VMD_choosing_optimal_K.ipynb` – Tuning the number of VMD components

### Data Wrangling
- `bitcoin_wrangling_1/2/3.ipynb` – Preprocessing 1-minute BTC data
- `Macro_wrangling.ipynb` – Cleaning macroeconomic and sentiment data

### Robustness
- `Robustness Checks/` – Additional notebooks testing different sample splits and reduced training data

### Local Training Versions
- `Local_GRU_1.ipynb`, `Local_GRU_2.ipynb` – GRU notebooks adapted for local execution with lower RAM use

---

## Tools & Techniques

- Python (Pandas, NumPy, Statsmodels, Scikit-learn, TensorFlow, TA-Lib)
- GRU (Gated Recurrent Unit)
- Variational Mode Decomposition (VMD)
- Self-Attention Mechanism
- Statistical time-series testing
- Forecast accuracy metrics (MAE, RMSE)

---

## Key Findings

| Model                          | Test MAE | Test RMSE |
|-------------------------------|----------|-----------|
| Naïve Benchmark               | 0.0476   | 0.0749    |
| ARIMA                         | 0.0476   | 0.0749    |
| GRU (basic)                   | 0.0480   | 0.0749    |
| GRU (with macro/sentiment)    | 0.0478   | 0.0749    |
| VMD-AttGRU (from literature)  | 0.0457   | 0.0703    |
| **VMD-GRU-Attention (proposed)** | **0.0158** | **0.0239** |

The **VMD-GRU-Attention model** considerably outperformed all others with high accuracy, suggesting that short-term Bitcoin returns in 2024 are **not fully random**, and that **potentially exploitable trading opportunities** may exist within the bitcoin market.

---

## Disclaimer

- The dataset used is public but **not included** due to size.
- This codebase is intended for **academic use only**.
- Please cite the dissertation if you use any part of this project in your own research.



