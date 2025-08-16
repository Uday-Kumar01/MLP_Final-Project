# Stock Price Prediction using Hybrid CNN-LSTM with ARIMA Contribution

## Project Description
This repository reproduces and extends the paper:
**“Attention-based CNN-LSTM and XGBoost Hybrid Model for Stock Prediction.”**  
Paper: https://arxiv.org/abs/2204.02623

The project is organized into two notebooks:
1. **Research Paper Code.ipynb** — Base implementation following the original methodology.
2. **Contributed Code.ipynb** — Our contribution where **ARIMA** preprocessing is added before the CNN–LSTM (with Attention) stage.

---

## Group Contribution
We introduce **ARIMA (Auto-Regressive Integrated Moving Average)** as an additional preprocessing step:
- Removes noise and trend from raw prices to improve stationarity.
- Supplies cleaner residual/processed signals to **CNN-LSTM + Attention**.
- Demonstrates value of combining classical time-series modeling with deep learning for financial forecasting.

---

## Repository Contents
- `Research Paper Code.ipynb` — Reproduction notebook.
- `Contributed Code.ipynb` — ARIMA-enhanced pipeline on a new 5-year stock dataset.
- `README.md` — This guide.

---

## Requirements
Tested on Python **3.7.4** with:
numpy==1.16.5
pandas==0.25.1
scikit-learn==0.21.3
statsmodels==0.10.1
tensorflow==2.1.0
keras==2.3.1
xgboost==1.5.0
matplotlib==3.1.1

## Usage
1. **Clone repo and open notebooks** in Jupyter or Google Colab.
2. Run either flow:
   - **Base paper:** open `Research Paper Code.ipynb` and run all cells.
   - **Contribution (ARIMA):** open `Contributed Code.ipynb` and run all cells.
3. Plots and metrics (RMSE/MAE and residual diagnostics) are saved/displayed within the notebooks.

---

## Data
- Original paper uses Chinese A-share data (e.g., TuShare); this repo also demonstrates on a **new 5-year stock dataset** to test generalization.
- Ensure your CSV contains at least: `Date, Open, High, Low, Close, Volume` (column names can be mapped in the notebook).

---

## Results Summary (brief)
- ARIMA preprocessing produced **cleaner residuals** (confirmed by ADF/Ljung–Box) and **lower prediction error** compared to the baseline CNN-LSTM alone.
- The method tracked long-term trends better on the 5-year dataset, showing improved robustness across different market phases.

---

## How to Cite the Paper
@article{shi2022attclx,
author = {Zhuangwei Shi and Yang Hu and Guangliang Mo and Jian Wu},
title = {Attention-based CNN-LSTM and XGBoost hybrid model for stock prediction},
journal = {arXiv preprint arXiv:2204.02623},
year = {2022}
}
