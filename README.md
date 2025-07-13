# 📈 Market Efficiency of Bitcoin in 2024

This repository contains the full code for my undergraduate dissertation:  
**"Market Efficiency of Bitcoin in 2024: Evidence from Statistical and Deep Learning Models"**,  
submitted for EC331: Research in Applied Economics at the University of Warwick.

📄 Full paper: *See dissertation PDF in repo root*

---

## 🧠 Overview

This study investigates the **weak form Efficient Market Hypothesis (EMH)** in the Bitcoin market by analysing **1-minute BTC/USD data from 2024**. I apply both **traditional statistical tests** and **state-of-the-art deep learning models**, including a novel **VMD-GRU-Attention** architecture.

Despite extensive volatility in Bitcoin prices, I find evidence of **predictable patterns**, especially when using advanced hybrid models—challenging the weak form EMH.

---

## 🔍 Research Questions

- Does the Bitcoin market in 2024 exhibit weak form efficiency?
- Can deep learning models forecast high-frequency Bitcoin returns more accurately than traditional econometric models?

---

## 🗂️ Repository Structure

This repo includes all Jupyter notebooks used in the dissertation:

### 📊 Statistical Testing
- `Statistical_tests.ipynb` – Ljung-Box, Runs test, Variance Ratio, Hurst exponent, BDS test

### 🔁 Econometric & Deep Learning Models
- `ARIMA.ipynb` – ARIMA(1,0,2) forecasting model
- `GRU_1.ipynb` – GRU model using only price and technical indicators
- `GRU_2.ipynb` – GRU model including macroeconomic and sentiment data
- `VMD_AttGRU.ipynb` – Benchmark: attention-before-GRU model (from literature)
- `VMD_GRU_Attention.ipynb` – Proposed model: GRU-before-attention
- `VMD_choosing_optimal_K.ipynb` – Tuning the number of VMD components

### 🧹 Data Wrangling
- `bitcoin_wrangling_1/2/3.ipynb` – Preprocessing 1-minute BTC data
- `Macro_wrangling.ipynb` – Cleaning macroeconomic and sentiment data

### ✅ Robustness
- `Robustness Checks/` – Additional notebooks testing different sample splits and reduced training data

### 🖥️ Local Training Versions
- `Local_GRU_1.ipynb`, `Local_GRU_2.ipynb` – GRU notebooks adapted for local execution with lower RAM use

---

## ⚙️ Tools & Techniques

- Python (Pandas, NumPy, Statsmodels, Scikit-learn, TensorFlow, TA-Lib)
- GRU (Gated Recurrent Unit)
- Variational Mode Decomposition (VMD)
- Self-Attention Mechanism
- Statistical time-series testing
- Forecast accuracy metrics (MAE, RMSE)

---

## 📌 Key Findings

| Model                | Test MAE | Test RMSE |
|---------------------|----------|-----------|
| Naïve Benchmark     | 0.0476   | 0.0749    |
| ARIMA               | 0.0476   | 0.0749    |
| GRU (basic)         | 0.0480   | 0.0749    |
| GRU (with macro/sentiment) | 0.0478 | 0.0749    |
| **VMD-GRU-Attention** | **0.0158** | **0.0239** |

The **VMD-GRU-Attention model** dramatically outperformed all others, indicating that short-term Bitcoin returns in 2024 are **not fully random**.

---

## ❗ Disclaimer

- 📦 The dataset used is public but **not included** due to size.
- 📚 This codebase is intended for **academic use only**.
- Please cite the dissertation if you use any part of this project in your own research.

---

## 🙏 Acknowledgements

Supervised by **Dr. Jeisson Cárdenas-Rubio**  
Special thanks to **Dr. Zeynep Kurter** and **Dr. Nathan Canen**


