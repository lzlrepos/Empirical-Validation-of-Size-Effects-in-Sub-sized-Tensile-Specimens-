# Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials


## Overview

This repository accompanies our research on the **mechanical behavior of sub-sized tensile specimens**, specifically focusing on **stainless steel 316 (SS316)**. The study presents:
- The largest known **open-access database** of tensile properties from sub-sized specimens,
- Empirical validation of **analytical models** (Barba’s law, Bertella-Oliver formula),
- Development of **machine learning (ML)** models for predictive modeling,
- Implementation of **uncertainty quantification (UQ)** methods to estimate confidence in predictions,
- Use of **SHAP (SHapley Additive exPlanations)** to interpret and explain feature importance in ML predictions,
- A comprehensive investigation into **specimen size effects** and validation of associated physical thresholds.


---

We developed a public dataset comprising 1,050 sub-sized tensile test records from nuclear structural materials. Using this dataset, we benchmarked various machine learning models—including Random Forest, XGBoost, and Gaussian Process Regression—to predict key tensile properties: yield strength (YS), ultimate tensile strength (UTS), uniform elongation (UE), and total elongation (TE). We also implemented uncertainty quantification using Bayesian Neural Networks and Natural Gradient Boosting. In addition, we validated existing analytical models and proposed refined critical values for specimen size effect thresholds. To better understand model predictions, we employed SHAP explainability to identify the most influential factors affecting tensile behavior.

---

## 📂 Repository Organization
- **Figures:**  contains codes related to the application of Machine Learning methods for predicting tensile properties in Figure 2 and Figure 3.<br>
  k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Tree, Random Forest (RF), XGBoost, Gaussian Process Regression (GPR), Artificial Neural Network (ANN)

- **Tables:**  contains codes related to the application of Machine Learning methods for predicting tensile properties and uncertainty quantification in Table 3, Table 4, Table 5 and Table 6.<br>
  k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Tree, Random Forest (RF), XGBoost, Gaussian Process Regression (GPR), Artificial Neural Network (ANN)
  Quantile Regression, NGBoost (Natural Gradient Boosting), Monte Carlo Dropout, Deep Ensemble, Bayesian Neural Network (Variational Inference), and Bayesian Neural Network (MCMC sampling)

---

## Machine Learning Models
| Model Type                 | Task                                | Models Used                                                                 |
|---------------------------|-------------------------------------|------------------------------------------------------------------------------|
| Regression       | Predict YS, UTS, UE, TE             | k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Trees, Random Forest, Extreme Gradient Boosting (XGBoost), Gaussian Process Regression (GPR), Artificial Neural Network (ANN) |
| Uncertainty Quantification| Estimate confidence in predictions  | Quantile Regression, Natural Gradient Boosting (NGBoost), Gaussian Process Regression (GPR), Deep Ensemble, Monte Carlo Dropout (MC Dropout), Bayesian Neural Networks (Variational Inference), Bayesian Neural Networks (MCMC) |


## 📊 Data and Evaluation Metrics
The dataset comprises 1,050 tensile test records of sub-sized stainless steel 316 specimens collected from published literature. Each record includes 55 features spanning material type, specimen geometry, heat treatment, testing conditions, and measured mechanical properties. For model evaluation, point prediction models were assessed using the coefficient of determination (R²) and  and root-mean-square error (RMSE), while uncertainty quantification (UQ) models were evaluated based on the coverage probability of 95% confidence intervals. 


## 🔨 Requirements

keras  2.6.0  
tensorflow 2.6.0  
pyro-ppl 1.8.5  
torchbnn 1.2  
torch 2.0.1  
pandas 1.5.3  
numpy 1.23.5  
scikit-learn 1.2.2  





## ▶️ Use
The codes are provided as Jupyter Notebook files. To reproduce the results, run the .ipynb files. 



## 📜 Citation

If you use this dataset, code, or findings in your work, please cite:

**Li, L., Merickel, J. W., Tang, Y., Song, R., Rittenhouse, J. E., Vakanski, A., & Xu, F.**  
*Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials*.  
Manuscript in review, 2024.


```bibtex
@article{li2024sizeeffects,
  title     = {Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials},
  author    = {Li, Longze and Merickel, Jacob W. and Tang, Yujun and Song, Rui and Rittenhouse, Jacob E. and Vakanski, Aleksandar and Xu, Fei},
  journal   = {Manuscript in review},
  year      = {2024}
}

