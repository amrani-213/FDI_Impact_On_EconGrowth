# Foreign Direct Investment and Economic Growth in Algeria
## An ARDL Bounds Testing Approach (1990–2023)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Complete-success)]()

---

## 📌 Project Overview

This repository contains the complete empirical implementation of an econometric study examining the relationship between **Foreign Direct Investment (FDI)** and **economic growth** in Algeria using the **Autoregressive Distributed Lag (ARDL) Bounds Testing** framework.

The analysis investigates both **short-run dynamics** and **long-run equilibrium relationships** between FDI and GDP while accounting for key macroeconomic variables such as oil prices, trade openness, inflation, and gross capital formation.

The project is conducted in the context of Algeria's structural dependence on hydrocarbons and recurring exposure to external shocks, including the **COVID-19 pandemic**, which is explicitly modeled using a dummy variable.

---

## 🎯 Research Objectives

The study seeks to answer the following questions:

- Does FDI exert a **long-run cointegrated effect** on Algeria's economic growth?
- Are there **short-run dynamic effects** of FDI on GDP?
- How do **oil prices**, **trade openness**, and **macroeconomic stability** influence growth?
- Has the relationship between FDI and GDP remained **stable over time**?

---

## 🧠 Methodological Framework

### Why ARDL?

The **ARDL Bounds Testing approach** (Pesaran, Shin & Smith, 2001) is particularly suitable because:

- ✅ It accommodates variables integrated of order **I(0)** and **I(1)**
- ✅ It performs well with **small samples**
- ✅ It allows **simultaneous estimation** of short-run dynamics and long-run relationships
- ✅ It avoids **spurious regression** when properly specified

> **Note:** No variable integrated of order I(2) is included, ensuring full compliance with ARDL assumptions.

---

## 📊 Data Description

- **Frequency:** Annual
- **Period:** 1990–2023
- **Country:** Algeria

### Variables Used

| Variable | Description |
|----------|-------------|
| `log(Real GDP)` | Measure of economic growth |
| `FDI (% of GDP)` | Foreign direct investment inflows |
| `Inflation` | CPI inflation rate |
| `GCF (% of GDP)` | Gross capital formation |
| `Trade Openness` | (Exports + Imports) / GDP |
| `log(Oil Price)` | International crude oil price |
| `D2020` | COVID-19 dummy variable |

**Sources:** World Bank (WDI), Macrotrends, FRED (POILBREUSD)

---

## 🧪 Econometric Procedure

### 1️⃣ Unit Root Testing
- Augmented Dickey–Fuller (ADF)
- Constant and trend specifications
- AIC-based lag selection

### 2️⃣ ARDL Model Selection
- Maximum lag length = 2
- Optimal specification chosen using AIC

### 3️⃣ Bounds Test for Cointegration
- Testing for long-run equilibrium

### 4️⃣ Short-Run Dynamic Estimation
- Interpreting lagged effects
- COVID-19 shock control

### 5️⃣ Model Diagnostics
- Serial correlation
- Heteroskedasticity
- Normality of residuals

### 6️⃣ Stability Analysis
- Recursive Estimation Stability Tests (REST)

---

## 📈 Key Findings

### 🔹 Long-Run Relationship
- ❌ **No evidence of cointegration** between FDI and GDP
- FDI does not appear to drive sustained long-run growth in Algeria (1990–2023)

### 🔹 Short-Run Dynamics
- FDI effects are **weak, unstable**, and marginally significant at best
- **Oil prices** exert a strong and delayed positive effect
- **Trade openness** shows negative lagged effects
- **COVID-19** caused a significant GDP contraction

### 🔹 Structural Insight
The Algerian economy remains:
- Highly dependent on **hydrocarbon revenues**
- Vulnerable to **external shocks**
- Limited in its ability to **transform FDI into durable growth**

---

---

## 🛠️ Technologies Used

- **Python 3.8+**
- **pandas** - Data manipulation
- **numpy** - Numerical computations
- **statsmodels** - Econometric modeling
- **matplotlib** & **seaborn** - Visualization
- **arch** - ARCH/GARCH models
- **scipy** - Statistical tests

---

## 📚 References

- Pesaran, M. H., Shin, Y., & Smith, R. J. (2001). *Bounds testing approaches to the analysis of level relationships*. Journal of Applied Econometrics, 16(3), 289-326.
- Dickey, D. A., & Fuller, W. A. (1979). *Distribution of the estimators for autoregressive time series with a unit root*. Journal of the American Statistical Association, 74(366a), 427-431.
- Gujarati, D. N., & Porter, D. C. (2009). *Basic Econometrics*. McGraw-Hill Education.
- World Bank – World Development Indicators
- Louail, B., Benanaya, D., & Bakdi, A. (2017). Foreign Direct Investment and Economic Growth in Algeria. *International Journal of Economics and Finance*, 9(4).

---

## 👤 Author

**Amrani Bouabdellah**  
Master's Student – Statistics & Data Science  
ENSSEA (Algeria)  
📧 abdouugk@gmail.com 
🔗 (https://github.com/amrani-213) 
---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- World Bank for data availability
- The econometrics community for open-source tools

---


---

**⭐ If you find this project useful, please consider giving it a star!**
