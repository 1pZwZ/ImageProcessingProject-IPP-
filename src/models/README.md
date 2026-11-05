# 🤖 Stage 5: Classification & Deep Learning Benchmarking (`src/models/`)

> **Lead Specialist:** Saad Abdulaziz Alshehri (`2240006495`)  
> **Role:** Machine Learning & CNN Developer

---

## 🎯 Module Objectives

This module trains and benchmarks two paradigms of plant leaf disease classification—classical machine learning on handcrafted DIP features versus end-to-end deep learning:

1. **Classical Machine Learning Classifiers (Target F1-Score $\ge 94\%$):**
   - **Support Vector Machine (SVM):** Trained on fused Color + GLCM + HOG feature vectors using RBF/linear kernels and hyperparameter tuning.
   - **Random Forest (RF):** Ensemble of decision trees trained on the multi-modal DIP features, providing feature importance rankings across texture, color, and gradient descriptors.
2. **Deep Learning Baseline (Target F1-Score $\ge 98\%$):**
   - **Fine-Tuned MobileNetV2:** Transfer learning using a pretrained MobileNetV2 backbone with a custom classification head for the 38 PlantVillage categories, trained with GPU acceleration on Google Colab.

---

## 🛠️ Planned Components

- `classical_classifiers.py` — Training, cross-validation, and inference pipelines for SVM and Random Forest (`scikit-learn`).
- `mobilenet_cnn.py` — PyTorch MobileNetV2 architecture definition, transfer learning fine-tuning loop, and GPU inference wrapper.

