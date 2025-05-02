# Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials


## Overview

This repository accompanies our research on the **mechanical behavior of sub-sized tensile specimens**, specifically focusing on **stainless steel 316 (SS316)**. The study presents:
- The largest known **open-access database** of tensile properties from sub-sized specimens,
- Empirical validation of **analytical models** (Barba’s law, Bertella-Oliver formula),
- Development of **machine learning (ML)** models for predictive modeling,
- Implementation of **uncertainty quantification (UQ)** methods to estimate confidence in predictions,
- Comprehensive investigation into **specimen size effects**.

---

## 🔍 Key Contributions

- ✅ Developed a public dataset of **1,050 sub-sized tensile test records** from nuclear structural materials
- ✅ Benchmarked **ML models** (Random Forest, XGBoost, GPR, etc.) to predict:
  - Yield Strength (YS)
  - Ultimate Tensile Strength (UTS)
  - Uniform Elongation (UE)
  - Total Elongation (TE)
- ✅ Applied **Bayesian Neural Networks** and **Natural Gradient Boosting** for UQ
- ✅ Validated analytical models and established **improved critical values** for size effect thresholds
- ✅ Used **SHAP explainability** to identify key factors affecting tensile behavior

---

## 📊 Dataset

- 📍 Source: Peer-reviewed publications
- 📈 Records: 1,050
- 📂 Parameters: 55 per record (material, dimensions, treatment, test conditions, etc.)
- 🔗 Available at: [Materials Cloud Repository](https://github.com/avakanski/Subsized-Specimens-Tensile-Properties)

---

## 🧠 Machine Learning Models

| Model Type               | Task                      | Best Model                        |
|--------------------------|---------------------------|-----------------------------------|
| Regression (point)       | YS, UTS, UE, TE prediction| Random Forest, XGBoost, GPR       |
| Uncertainty Quantification | UQ for all properties     | NGBoost, BNN-MCMC, GPR            |

- ML Libraries used: `scikit-learn`, `xgboost`, `catboost`, `ngboost`, `PyTorch`, `Pyro`
- UQ methods include: Quantile Regression, Bayesian Neural Networks, Deep Ensemble, MC Dropout

---

## 🧪 Analytical Model Validation

- **Barba’s Law** and **Bertella-Oliver formula** were evaluated using our data.
- Bertella-Oliver yielded better fit (R² = 0.54), but both are sensitive to test conditions.
- ML models substantially outperformed analytical models in predictive accuracy.

---

## 🔎 Specimen Size Effect Findings

| Hypothesis Tested | Conclusion |
|-------------------|------------|
| Thickness < 0.2 mm affects properties | ✅ Confirmed |
| Thickness-to-grain-size ratio ≥ 10 required | ✅ Confirmed |
| Slenderness ratio affects TE, UE | ✅ Confirmed (TE decreases with slenderness) |
| Width-to-thickness ratio affects UTS, TE | ✅ Confirmed above critical value of 5 |

---

## 📌 Feature Importance (SHAP)

- Most important features for prediction:
  1. **Specimen treatment**
  2. **Test temperature**
  3. Specimen geometry (thickness, width)
  4. Grain size

---

## 📁 Repository Structure (Suggested)

