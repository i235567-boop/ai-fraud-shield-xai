# Bridging the Trust Gap in Financial Fraud Detection 🤖🔒

### An Explainable AI Framework for Regulatory Compliance

**A Research Paper by Sumyyah Saeed** *Department of Financial Technologies, FAST National University of Computer and Emerging Sciences, Islamabad*

<div align="center">

[![Paper](https://img.shields.io/badge/📄-Research_Paper-blue.svg)](https://drive.google.com/file/d/111tvt2MyBlI5vyY5CQ-doZB7irjUnhp3/view?usp=sharing)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Cb4ooD7PDZSxJQtuheCi23SMaNFBjp-L?usp=sharing)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-blue?logo=kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
[![GitHub](https://img.shields.io/badge/💻-Code_Repository-black?logo=github)](https://github.com/i235567-boop/ai-fraud-shield-xai)
[![LinkedIn](https://img.shields.io/badge/🔗-LinkedIn_Post-0A66C2)](https://www.linkedin.com/posts/sumyyah-saeed-b5381128b_xai-for-fraud-detection-sumyyah-saeed-activity-7458222096070942720-VEDv?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEZr7i8B0ACD7izF5NgTdUASou0y360WUfY)
[![Website](https://img.shields.io/badge/🌐-Project_Showcase_Site-4285F4)](https://sites.google.com/isb.nu.edu.pk/ai-fraud-shield/home)

</div>

---

## 📖 Overview

Financial fraud detection systems face a fundamental conflict: achieving high classification accuracy while meeting the strict transparency obligations of emerging global laws like the **EU AI Act**. Traditional "black-box" models excel at catching fraud but fail to explain *why*, creating a significant barrier to legal deployment and user trust.

This research proposes and validates a **two-phase explainable ensemble learning framework**. By integrating SMOTE for imbalance handling, a hierarchical stacking ensemble (Random Forest + XGBoost), and dual post-hoc interpretability layers (**SHAP** and **LIME**), we prove that regulatory transparency and high-performance fraud detection are **simultaneously achievable**.

The best model (Random Forest) achieved an **F1 Score of 0.8586**, **Precision of 0.8817**, and correctly identified **82 of 98 fraud cases** while generating only 11 false alarms.

---

## 🎯 Key Contributions

- ✅ **Regulatory-Aligned Framework:** A stacking ensemble with dual SHAP & LIME layers that produces EU AI Act-compliant transparency records.
- ✅ **Rigorous Experimental Design:** A 24-configuration protocol crossing 4 model types, 3 feature selection strategies, and 2 resampling conditions.
- ✅ **No Data Leakage:** A strict two-phase pipeline isolates model selection from explainability generation.
- ✅ **Attribution-Based Selection:** Empirically validated SHAP-based feature selection against traditional Pearson correlation.
- ✅ **Instance-Level Audit Records:** Generated LIME outputs that satisfy the requirement for individualized explanations.

---

## 🧠 Methodology (High-Level)

The framework operates in two distinct phases:

1. **Phase 1: Model Selection.** Train and evaluate 24 configurations to find the best-performing model.
2. **Phase 2: Compliance Generation.** Apply SHAP (global) and LIME (local) *exclusively* to the best model to generate audit-ready documentation.

**Key Components:**
* **Data Preprocessing:** Log transformation + Z-score normalization of `Amount` and `Time`.
* **Imbalance Mitigation:** SMOTE applied only to the training set (578:1 → 1:1 balance).
* **Ensemble Models:** Logistic Regression (baseline), Random Forest, XGBoost, and a Stacking Ensemble.
* **Explainability:** SHAP for global feature importance, LIME for local, instance-level predictions.

---

## 📊 Results Snapshot

| Model | F1 Score | ROC-AUC | Precision | Recall |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest (Best F1)** | **0.8586** | 0.9794 | **0.8817** | **0.8367** |
| Stacking Ensemble (Best AUC) | 0.8410 | **0.9838** | 0.8454 | 0.8367 |
| XGBoost | 0.7736 | 0.9806 | 0.7193 | 0.8367 |
| Logistic Regression | 0.1088 | 0.9696 | 0.0578 | 0.9184 |

**Operational Impact (Random Forest on 56,962 test transactions):**
* ✅ **True Positives:** 82 (Fraud caught)
* ❌ **False Negatives:** 16 (Fraud missed)
* ✅ **True Negatives:** 56,853 (Legit transactions cleared)
* ❌ **False Positives:** 11 (Legit transactions wrongly blocked)

---

## 🔗 Project Links & Resources

| Resource | Link |
| :--- | :--- |
| 📁 **GitHub Repository** | [github.com/i235567-boop/ai-fraud-shield-xai](https://github.com/i235567-boop/ai-fraud-shield-xai) |
| 📊 **Dataset (Kaggle)** | [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |
| 🚀 **Google Colab Notebook** | [Open in Colab](https://colab.research.google.com/drive/1Cb4ooD7PDZSxJQtuheCi23SMaNFBjp-L?usp=sharing) |
| 🔗 **LinkedIn Post** | [Sumyyah Saeed's Post](https://www.linkedin.com/posts/sumyyah-saeed-b5381128b_xai-for-fraud-detection-sumyyah-saeed-activity-7458222096070942720-VEDv?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEZr7i8B0ACD7izF5NgTdUASou0y360WUfY) |
| 🌐 **Project Showcase Site** | [Google Site](https://sites.google.com/isb.nu.edu.pk/ai-fraud-shield/home) |

---

## 🧪 Reproducing the Experiments

To replicate this research:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/i235567-boop/ai-fraud-shield-xai.git
   cd ai-fraud-shield-xai
   ```
2. **Access the Data:** Download `creditcard.csv` from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and place it in the `/data` directory.
3. **Run the Notebook:** Open the provided Google Colab link or run the Jupyter notebook locally.
4. **View Results:** The notebook generates ROC curves, PR curves, SHAP beeswarm plots, and LIME explanations automatically.

---

## 📚 Citation

If you use this framework or reference this research, please cite:

```bibtex
@article{saeed2025bridging,
  title={Bridging the Trust Gap in Financial Fraud Detection: An Explainable AI Framework for Regulatory Compliance},
  author={Saeed, Sumyyah},
  journal={Department of Financial Technologies, FAST NUCES},
  year={2025}
}
```

---

## 👩‍💻 Author & Acknowledgements

**Author:** **Sumyyah Saeed** *BS in Financial Technology, FAST National University of Computer and Emerging Sciences, Islamabad*

**Supervisor:** **Dr. Usama Arshad** *My most sincere and profound gratitude to Dr. Arshad for his invaluable instructional guidance and mentorship throughout this research.*

**Acknowledgments:** * The Machine Learning Group at Université Libre de Bruxelles for the Kaggle dataset.
* The open-source communities behind SHAP, LIME, Scikit-learn, and XGBoost.

---

## 📜 License & Status

This project is for academic and research purposes. The code is available under the **MIT License**.

**Status:** ✅ Research Complete | 📄 Paper Published | 🧪 Code & Results Public
