# 📐 Stage 4: Multi-Modal Feature Extraction (`src/features/`)

> **Lead Specialists:**  
> - **Faisal Abdullah Alshehri** (`2240001737`) — *GLCM Texture & Color Moments*  
> - **Saad Abdulaziz Alshehri** (`2240006495`) — *HOG Shape/Gradient Descriptors & Feature Fusion*

---

## 🎯 Module Objectives

This module transforms segmented leaf lesions into compact, discriminative numerical feature vectors combining color, texture, and shape information:

1. **Color Moments:**
   - Compute 1st, 2nd, and 3rd order statistical moments (**Mean**, **Standard Deviation**, and **Skewness**) across RGB, HSV, and CIELAB channels within the segmented lesion ROI.
2. **GLCM Texture Descriptors (Gray-Level Co-occurrence Matrix):**
   - Compute spatial gray-level co-occurrence matrices across multiple distances ($d \in \{1, 2, 3\}$) and orientations ($\theta \in \{0^\circ, 45^\circ, 90^\circ, 135^\circ\}$).
   - Extract Haralick texture properties: **Contrast**, **Correlation**, **Energy (Angular Second Moment)**, and **Homogeneity**.
3. **HOG Descriptors (Histogram of Oriented Gradients):**
   - Compute local gradient orientation histograms to capture lesion shape, margin irregularity, and venation patterns.
4. **Feature Vector Fusion:**
   - Concatenate and normalize Color Moments + GLCM + HOG descriptors into a unified multi-modal feature vector for classical machine learning classifiers.

---

## 🛠️ Planned Components

- `color_features.py` — Color moments (mean, std, skewness) and color histogram descriptors.
- `glcm_texture.py` — GLCM matrix construction and contrast, correlation, energy, and homogeneity extraction.
- `hog_descriptors.py` — HOG feature computation and visualization.
- `feature_pipeline.py` — Multi-modal feature concatenation, standardization (`StandardScaler`), and caching.

