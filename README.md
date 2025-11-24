# 🇬🇧 Forecasting CO₂ Emissions per Capita in the United Kingdom  
### A Complete Time-Series Modeling Pipeline Using ARIMA & the Box–Jenkins Methodology

## 🎯 Project Overview

This repository contains a full end-to-end **time-series forecasting project** focused on modeling and forecasting **per-capita CO₂ emissions in the United Kingdom (1850–2023)**.

The goal of this project is to:

- Understand long-term emissions patterns.
- Apply rigorous time-series methodology to obtain a statistically robust model.
- Generate 3-year forecasts (2024–2026).
- Evaluate model performance using real historical data.
- Connect insights to **UN Sustainable Development Goal 13 (Climate Action)**.

This project combines **exploritory data analysis, stationarity testing, model identification, diagnostics, and forecasting**, fully documented in a **Jupyter Notebook** and a **PDF report**.

---

## 📋 Table of Contents

- [Problem Statement](#problem-statement)
- [Dataset Summary](#dataset-summary)
- [Methodology](#methodology)
- [Exploratory Analysis](#exploratory-analysis)
- [Time-Series Modeling](#time-series-modeling)
- [Model Evaluation](#model-evaluation)
- [Forecast Results](#forecast-results)
- [Repository Structure](#repository-structure)
- [Tech Stack](#tech-stack)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [CV Bullet Points](#cv-bullet-points)

---

## 🎓 Problem Statement

The United Kingdom has undergone significant transformations in industrial activity, energy consumption, and sustainability policy over the last 170+ years. Understanding the **historical behavior of CO₂ emissions per capita** and forecasting **future levels** is essential for:

- Environmental policy development  
- Tracking national sustainability progress  
- Supporting climate-action strategies  
- Monitoring alignment with **SDG 13: Climate Action**  

This project applies **rigorous statistical forecasting techniques** to generate meaningful predictions and insights.

---

## 📊 Dataset Summary

**Source:** Our World in Data – CO₂ emissions per capita  
**Years:** 1850–2023 (174 annual observations)  
**Variable:**  
- `co2_per_capita` — Tonnes of CO₂ per person  

**Key notes:**

- Long-term structural trend (non-stationary)
- No seasonality (annual data)
- Retained all data points (no artificial outlier removal)

---

## 🧪 Methodology

The workflow follows the **Box–Jenkins time-series modeling framework**:

1. Exploratory Data Analysis  
2. Stationarity Checks  
   - Decomposition  
   - ADF Test  
3. Differencing  
4. Model Identification (ACF/PACF)  
5. ARIMA Model Selection (AIC optimization)  
6. Model Diagnostic Checks  
7. Train/Test Evaluation  
8. Forecasting Future Values  

Final selected model:

> **ARIMA(2, 1, 6)** — chosen based on lowest AIC and strongest diagnostic results.

---

## 🔍 Exploratory Analysis

### Descriptive Statistics
- Distribution analysis  
- Quartiles, mean, and standard deviation  
- Detection of structurally meaningful outliers  

### Outlier Analysis
Methods applied:

- Z-score (threshold ±3)
- IQR-based rule (1.5 × IQR)

All potential outliers were **kept**, as they represent historical transitions (WWII, industrial shifts, decarbonization policies).

### Time-Series Behavior

- Strong upward trend during the industrialization era  
- Mid-20th-century peak  
- Long-term decline due to clean-energy policies and efficiency improvements  

---

## ⏱️ Time-Series Modeling

### Stationarity Testing

- Series is **non-stationary** (ADF p-value > 0.05)
- **First-order differencing** applied  
- Differenced series passed visual and statistical checks  

### Model Identification

ACF/PACF patterns suggested a mix of AR and MA components.  
Several ARIMA(p,1,q) models were tested.

### Final Model: **ARIMA(2, 1, 6)**

Reasons for selection:

- Best AIC score  
- Strong residual white-noise behavior  
- No autocorrelation in residuals  
- Residuals approximate normal distribution  

### Diagnostic Checks

- Residual ACF → no significant spikes  
- QQ-plot → near-linear behavior  
- Ljung–Box test → fails to reject independence  

---

## 🧮 Model Evaluation

### Train/Test Split (80/20)

**Performance Metrics:**  
- **MAE:** 1.463  
- **MAPE:** 24.76%  
- **Residual bias:** ≈ 0  

The model performs well for long-term forecasting of environmental indicators.

---

## 📈 Forecast Results (2024–2026)

The model predicts a **continued decline in per-capita CO₂ emissions**, reflecting:

- Clean-energy adoption  
- Energy-efficiency improvements  
- Decarbonization policies  

The notebook includes:

- Point forecasts  
- 95% confidence intervals  
- Forecast visualization (trend + uncertainty)  
