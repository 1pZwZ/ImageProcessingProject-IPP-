# 🎨 Stage 2: Color Space Segmentation (`src/segmentation/`)

> **Lead Specialist:** Mohammed Nasser Al-Marhoon (`2240005893`)  
> **Role:** Color Segmentation Lead

---

## 🎯 Module Objectives

This module isolates diseased leaf tissue from healthy green foliage and background using perceptual color space transformations and unsupervised clustering/thresholding:

1. **Color Space Transformation:**
   - Convert preprocessed RGB images into **HSV (Hue, Saturation, Value)** and **CIELAB ($L^*a^*b^*$)** color spaces.
   - Utilize the **$a^*$ chrominance channel** (red-green axis in CIELAB) and **Hue/Saturation channels** (in HSV) to decouple chromatic disease cues (yellowish-brown chlorotic and necrotic spots) from lighting variations.
2. **K-Means Color Clustering ($k=3$):**
   - Partition pixels in the transformed color space into $k=3$ clusters corresponding to:
     1. Image background
     2. Healthy green leaf tissue
     3. Infected disease lesions
3. **Otsu Adaptive Thresholding:**
   - Apply automatic global/local **Otsu thresholding** on the $a^*$ and Saturation channels to generate candidate lesion masks and compare/combine with K-means cluster masks.

---

## 🛠️ Planned Components

- `color_spaces.py` — RGB $\rightarrow$ HSV and RGB $\rightarrow$ CIELAB ($L^*a^*b^*$) conversions and channel extraction helpers.
- `kmeans_segmenter.py` — K-means clustering ($k=3$) on $(a^*, b^*)$ and $(H, S)$ feature spaces with automatic lesion cluster selection.
- `otsu_thresholding.py` — Otsu thresholding and hybrid mask generation.

