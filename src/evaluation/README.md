# 📊 Stage 6: Evaluation & Visualization (`src/evaluation/`)

> **Lead Specialist:** Mohammed Sameer Alajlan (`2240002025`)  
> **Role:** Evaluation & Visualization Lead

---

## 🎯 Module Objectives

This module provides rigorous quantitative and qualitative evaluation of both the segmentation pipeline and the disease classifiers:

1. **Classification Metrics:**
   - **Overall Accuracy**, **Macro/Weighted Precision**, **Recall (Sensitivity)**, **F1-Score**, and **ROC-AUC**.
   - Multi-class **Confusion Matrices** to diagnose specific inter-class misclassifications across the 38 crop-disease categories.
2. **Segmentation Quality Metrics:**
   - **Intersection over Union (IoU / Jaccard Index)** and **Dice Similarity Coefficient** to evaluate the accuracy of K-means/Otsu + morphological lesion masks.
3. **Computational Efficiency Benchmarks:**
   - Measure **Inference Speed (ms/image)**, **Model Size (MB)**, and **Memory Footprint** comparing SVM, Random Forest, and MobileNetV2.
4. **Publication-Ready Visualizations:**
   - Multi-panel pipeline progression figures (Raw $\rightarrow$ Filtered/CLAHE $\rightarrow$ CIELAB $a^*$ $\rightarrow$ K-means/Otsu $\rightarrow$ Morphological Mask $\rightarrow$ Prediction).

---

## 🛠️ Planned Components

- `metrics.py` — Classification metrics (Accuracy, Precision, Recall, F1, ROC-AUC) and segmentation metrics (IoU, Dice).
- `benchmark.py` — Inference latency timer (ms/image), parameter count, and memory footprint profiler.
- `visualize.py` — Confusion matrix heatmaps, ROC curves, feature importance bar charts, and side-by-side DIP pipeline stage visualizers.

