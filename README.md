# Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials


## Overview

This repository accompanies our research on the **mechanical behavior of sub-sized tensile specimens**, specifically focusing on **stainless steel 316 (SS316)**. The study presents:
- The largest known **open-access database** of tensile properties from sub-sized specimens,
- Empirical validation of **analytical models** (Barba’s law, Bertella-Oliver formula),
- Development of **machine learning (ML)** models for predictive modeling,
- Implementation of **uncertainty quantification (UQ)** methods to estimate confidence in predictions,
- Comprehensive investigation into **specimen size effects**.

---

We developed a public dataset comprising 1,050 sub-sized tensile test records from nuclear structural materials. Using this dataset, we benchmarked various machine learning models—including Random Forest, XGBoost, and Gaussian Process Regression—to predict key tensile properties: yield strength (YS), ultimate tensile strength (UTS), uniform elongation (UE), and total elongation (TE). We also implemented uncertainty quantification using Bayesian Neural Networks and Natural Gradient Boosting. In addition, we validated existing analytical models and proposed refined critical values for specimen size effect thresholds. To better understand model predictions, we employed SHAP explainability to identify the most influential factors affecting tensile behavior.

---

## 📊 Dataset: Tensile_Properties_Data.xlsx

- 📍 Source: Peer-reviewed publications
- 📈 Records: 1,050
- 📂 Parameters: 55 per record (material, dimensions, treatment, test conditions, etc.)


---

## 🧠 Machine Learning Models
| Model Type                 | Task                                | Models Used                                                                 |
|---------------------------|-------------------------------------|------------------------------------------------------------------------------|
| Regression (point)        | Predict YS, UTS, UE, TE             | k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Trees, Random Forest, Extreme Gradient Boosting (XGBoost), Gaussian Process Regression (GPR), Artificial Neural Network (ANN) |
| Uncertainty Quantification| Estimate confidence in predictions  | Quantile Regression, Natural Gradient Boosting (NGBoost), Gaussian Process Regression (GPR), Deep Ensemble, Monte Carlo Dropout (MC Dropout), Bayesian Neural Networks (Variational Inference), Bayesian Neural Networks (MCMC) |

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


## ▶️ Use
The codes are provided as Jupyter Notebook files. To reproduce the results, run the .ipynb files. 
