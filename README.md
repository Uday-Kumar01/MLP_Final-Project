# Stock Price Prediction using Hybrid CNN-LSTM with ARIMA Contribution

## Project Description
This repository contains the implementation of the research paper:  
**"Attention-CLX: Stock Prediction using Hybrid CNN-LSTM Model"**  
[Paper Link](https://arxiv.org/abs/2204.02623)

The project is divided into two parts:  
1. **Research Paper Code.ipynb** → Base implementation from the original paper.  
2. **Contributed Code.ipynb** → Group contribution where ARIMA was added as a preprocessing stage to improve prediction stability and capture time-series dependencies before feeding data into CNN–LSTM.

---

## Group Contribution
We introduced an **ARIMA (Auto-Regressive Integrated Moving Average)** model as an additional stage to the pipeline.  
- This helps analyze the **trend and stationarity** of stock price data.  
- Predictions from ARIMA were integrated with CNN-LSTM predictions for improved learning.  
- The contribution adds value by showing how classical statistical models can complement deep learning in financial forecasting.

---

## Files in this Repository
- `Research Paper Code.ipynb` → Original code reproduction.  
- `Contributed Code.ipynb` → Code with ARIMA contribution.  
- `README.md` → Documentation and usage guide.  

---

##  Requirements
Install the dependencies before running:  
```bash
pip install pandas numpy matplotlib statsmodels scikit-learn tensorflow keras
