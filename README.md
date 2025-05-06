# Empirical Validation of Size Effects in Sub-sized Tensile Specimens for Nuclear Structural Materials

[![Scientific Reports](https://img.shields.io/badge/Scientific_Reports-DOI%3A_10.1038%2Fs41598--024--61189--x-brightgreen.svg)](https://doi.org/10.1038/s41598-025-98849-5)  

## Overview
With the increasing need for mechanical characterization of small-scale components, particularly in scenarios where only limited material is available—such as in nuclear reactors—the study explores the role of machine learning (ML) in understanding and predicting specimen size effects in tensile testing. Traditional models and guidelines such as Miniaturized Tensile Test (MTT) have established practices for sub-sized specimens, but most prior studies relied on small datasets and analytical models with limited generalizability. To overcome these challenges, we constructed a comprehensive database of 1,050 tensile test records from peer-reviewed studies and introduced a machine learning framework capable of predicting key tensile properties like yield strength, ultimate tensile strength, and elongation for sub-sized specimens of stainless steel 316.

The study identifies a critical knowledge gap in the generalizability and uncertainty assessment of existing analytical approaches. Unlike traditional models that often require material-specific assumptions, the proposed ML models incorporate uncertainty quantification (UQ), which provides confidence intervals for predictions—a vital feature for high-stakes applications. Additionally, we validated current analytical models for correlating total elongation between sub-sized and standard-sized specimens, emphasizing the importance of experimental verification and robust data-driven methods. We also sheds light on the inherent variability in mechanical properties of sub-sized specimens, reinforcing the need for probabilistic modeling approaches.

Our work presents the first known application of ML to predict tensile properties from sub-sized specimens and demonstrates its advantages over traditional techniques through data-driven insights and UQ. We advocate for the continued development of large, open-source databases to advance the field and support more accurate, scalable predictions of mechanical properties in small-scale material testing.

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
| Regression       | Single-point estimates YS, UTS, UE, TE             | k-Nearest Neighbors (kNN), Support Vector Machine (SVM), Decision Trees, Random Forest, Extreme Gradient Boosting (XGBoost), Gaussian Process Regression (GPR), Artificial Neural Network (ANN) |
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

If you use the codes or the methods in your work, please cite the following <a href="https://doi.org/10.1038/s41598-025-98849-5">article</a>:   

    @article{li2025,
      TITLE= {Empirical validation of size effects in sub-sized tensile specimens for nuclear structural materials},
      AUTHOR= {Li, Longze and Merickel, John W. and Tang, Yalei and Song, Rongjie and Rittenhouse, Joshua E. and Vakanski, Aleksandar and Xu, Fei},
      JOURNAL = {Scientific Reports},
      YEAR = {2025},
      VOLUME = {15},
      ISSUE = {1},
      ARTICLE-NUMBER = {13846},
      URL = {https://doi.org/10.1038/s41598-025-98849-5},
      ISSN = {2045-2322},
      DOI = {10.1038/s41598-025-98849-5},
  }

## 🚩 License
<a href="License - MIT.txt">MIT License</a>


## 👏 Acknowledgments
This work was supported by the University of Idaho and Idaho National Laboratory. This work was also supported through the INL Laboratory Directed Research & Development (LDRD) Program under DOE Idaho Operations Office Contract. 

## ✉️ Contact or Questions
<a href="https://www.webpages.uidaho.edu/vakanski/">A. Vakanski</a>, e-mail: vakanski at uidaho.edu
