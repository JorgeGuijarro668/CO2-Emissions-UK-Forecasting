# CO₂ Emissions per Capita Forecast – United Kingdom

This repository contains a time series analysis and forecast of **CO₂ emissions per capita in the United Kingdom** using classical statistical modeling (ARIMA). The goal is to understand historical trends and generate short-term forecasts that help assess progress toward **SDG 13 – Climate Action**.

---

## Project Overview

The project:

- Uses historical annual CO₂ emissions per capita data for the United Kingdom.
- Performs exploratory data analysis (EDA) and outlier detection.
- Evaluates stationarity and identifies an appropriate ARIMA model via the Box–Jenkins methodology.
- Trains and validates an **ARIMA(2,1,6)** model.
- Produces 3-year forecasts with confidence intervals and visualizations.

All the analysis code is contained in a single Jupyter Notebook, and the accompanying PDF report summarizes the methodology, results, and policy implications.

---

## Repository Structure

```text
.
├─ CO2_emissions_UK.ipynb    # Main analysis notebook (EDA, modeling, forecasting)
├─ C02_EMISSIONS_UK.pdf      # Written report with methodology, figures and conclusions
└─ data/
   └─ uk_co2_per_capita.csv  # CO₂ emissions per capita for the United Kingdom
