# PEM-input-signal-Dynamism-metric-calculation
The code we propose in this repository calculates a Dynamism metric for input signals of PEM electrolysers. The Dynamism metric can also assist on both the definition of the experimental campaign and the transfer of the experimental accelerated results into the real conditions.
# ⚡ Dynamism Calculation for PEM Electrolyzer Input Signals

This repository provides tools in **MATLAB** and **Python** for calculating the **dynamism** of input signals applied to **PEM (Proton Exchange Membrane) electrolyzers**.  
Dynamism quantifies how variable or fluctuating a signal is — an important indicator for studying system performance, degradation, and durability under dynamic operating conditions.

---

## 📘 Overview

The scripts process voltage (or current/power) time-series data and calculate a set of **dynamism metrics** using the **Rainflow cycle counting** method.  
They then compare these metrics against experimental degradation data to explore relationships between signal variability and degradation rate.

Both implementations (`.mlx` and `.py`) provide equivalent functionality for:
- Signal preprocessing
- Rainflow cycle extraction
- Dynamism metric computation
- Visualization and regression analysis

---

## 🧮 Dynamism Metrics

Each signal is summarized using five primary metrics:

| Metric | Description |
|:--------|:-------------|
| **Mean voltage** | Average signal level |
| **Median amplitude** | Median Rainflow cycle amplitude |
| **Median period** | Median Rainflow cycle period |
| **Median positive dynamism** | Median positive amplitude/time ratio |
| **Median negative dynamism** | Median negative amplitude/time ratio |

An overall **Dynamism Index** is derived by normalizing and combining these metrics.

---

## 🧰 MATLAB Version (`dynamism_calculation.mlx`)

### Requirements
- MATLAB R2022a or later  
- Signal Processing Toolbox  
- Statistics and Machine Learning Toolbox  

### Usage
1. Open `dynamism_calculation.mlx` in MATLAB.
2. Use your own input signals (two columns of time and voltage current in excel)
3. Use your own degradation rates
4. The limits should be modified to normalise the results (depending the maximum values of range, periods,...) 
5. Load or edit the input signal (time, voltage/current).  
6. Run all sections to compute and visualize:
   - Dynamism metrics
   - Dynamism vs. degradation plots
   - Polynomial regression fitting (2nd order) could be another in your case

---

## 🐍 Python Version (`dynamism_calculation.py`)

### Requirements
Install dependencies via pip:
```bash
pip install numpy pandas matplotlib rainflow openpyxl
### Usage
1. Open `dynamism_calculation.py` in spyder.
2. Use your own input signals (two columns of time and voltage current in excel)
3. Use your own degradation rates
4. The limits should be modified to normalise the results (depending the maximum values of range, periods,...) 
5. Load or edit the input signal (time, voltage/current).  
6. Run all sections to compute and visualize:
   - Dynamism metrics
   - Dynamism vs. degradation plots
   - Polynomial regression fitting (2nd order) could be another in your case
