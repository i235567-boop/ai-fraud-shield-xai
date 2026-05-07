# Bridging the Trust Gap in Financial Fraud Detection: An Explainable AI Framework for Regulatory Compliance

**Author:** [Sumyyah Saeed](https://www.linkedin.com/in/sumyyah-saeed-b5381128b/)  
**Department:** Financial Technologies, FAST National University of Computer and Emerging Sciences, Islamabad, Pakistan  
**Supervisor:** Dr. Usama Arshad (to whom I am most grateful)

---

## 📌 Project Overview

[cite_start]This research addresses the fundamental conflict in financial fraud detection: the trade-off between **predictive accuracy** and **regulatory transparency**[cite: 1]. [cite_start]With emerging global laws like the **EU AI Act**, financial institutions require more than just accurate models; they need "audit-ready" documentation for high-risk AI decisions[cite: 2, 24].

This project proposes a two-phase framework that integrates:
1.  [cite_start]**Class Imbalance Mitigation:** Synthetic Minority Over-sampling (SMOTE)[cite: 3, 27].
2.  [cite_start]**Advanced Ensembles:** A hierarchical stacking ensemble combining Random Forest and XGBoost[cite: 3].
3.  [cite_start]**Dual-Layer XAI:** Post-hoc interpretability using **SHAP** (Global) and **LIME** (Local) to satisfy transparency obligations[cite: 3, 32].

## 🚀 Key Results

[cite_start]The framework was evaluated across 24 configurations using the Kaggle Credit Card Fraud benchmark (284,807 transactions)[cite: 4].

* [cite_start]**Best Balanced Performance:** **Random Forest** achieved the highest **F1 Score (0.8586)**, with 0.8817 precision and 0.9794 ROC-AUC[cite: 5].
* [cite_start]**Best Discrimination:** The **Stacking Ensemble** achieved the highest **ROC-AUC (0.9838)**[cite: 6].
* [cite_start]**Regulatory Compliance:** LIME produced fully interpretable, instance-level audit records satisfying **EU AI Act Article 13** requirements for individualized explanations[cite: 7, 32].


## 🛠️ Methodology

[cite_start]The pipeline is split into two sequential phases to prevent data leakage and ensure explanation stability[cite: 30, 96]:

### Phase 1: Model Development & Validation
* [cite_start]**Preprocessing:** Log transformation of transaction amounts and Z-score normalization[cite: 98, 103].
* [cite_start]**Resampling:** SMOTE applied strictly to the training set to preserve the authentic 0.172% fraud rate in testing[cite: 109, 110].
* [cite_start]**Feature Selection:** Comparison of SHAP-based attribution versus Pearson correlation[cite: 31, 105].

### Phase 2: Explainability & Transparency
* [cite_start]**SHAP (Global):** Identified **V14, V12, and V4** as the most influential fraud predictors across the dataset[cite: 6].
* [cite_start]**LIME (Local):** Generates feature weight vectors for individual fraud predictions to justify automated decisions to human auditors[cite: 18, 115].


## 🔗 Important Links

* **Code & Visualization:** [GitHub Repository](https://github.com/i235567-boop/ai-fraud-shield-xai)
* **Interactive Notebook:** [Google Colab Link](https://colab.research.google.com/drive/1Cb4ooD7PDZSxJQtuheCi23SMaNFBjp-L?usp=sharing)
* **Dataset Source:** [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* **Professional Networking:** [LinkedIn Post & Discussion](https://www.linkedin.com/in/sumyyah-saeed-b5381128b/)
* **Project Showcase:** [Google Site - Research Portfolio](https://sites.google.com/d/1-3ufTzeoSx11hNnsu8ELnHtrjxF4_G5M/p/1dIiIfVHEi_CDyTPqhF885HvGKkLUDB3d/edit)

## 🏗️ System Architecture

[cite_start]The proposed system ensures that regulatory transparency and competitive performance are simultaneously achievable within the same pipeline[cite: 8].


---
*Developed as part of BS Financial Technology at FAST NUCES.*
