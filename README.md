# LSTM vs TCN — Time Series Forecasting Comparison

##  Overview
This project compares two deep learning architectures — **LSTM (Long Short-Term Memory)** and **TCN (Temporal Convolutional Network)** — for **time series prediction**.  
The goal is to evaluate which model performs better in capturing temporal dependencies for forecasting air quality (PM2.5 and PM10 levels).

---

##  Features
- Multivariate time series forecasting  
- Sequence creation using sliding window (30 days input → 7 days output)  
- Model comparison based on accuracy and loss metrics  
- Visualisations for predictions, errors, and feature importance  
- Experiments with **normal** vs **biased** training (based on feature importance)

---

## Model Architectures

### 1. LSTM (Long Short-Term Memory)
- Captures long-term dependencies using gated recurrent units  
- Works sequentially — one time step after another  

### 2. TCN (Temporal Convolutional Network)
- Uses **causal convolutions** and **dilations** to model sequences  
- Parallelisable and often faster to train than LSTM  

---

## 📊Dataset
- Hourly air quality dataset for 5 years  
- Attributes: `date`, `pollution`, `dew`, `temperature`, `pressure`, `wind direction`, `wind speed`, `snow`, `rain`  
- Target variable: **pollution (PM2.5 or PM10)**  

---



---

## How to Run
```bash
# Clone this repository
git clone https://github.com/nradhakrishna/LSTM-vs-TCN.git
cd LSTM-vs-TCN

# Install dependencies
pip install -r requirements.txt

# Run the training notebook
jupyter notebook LSTM_vs_TCN.ipynb
