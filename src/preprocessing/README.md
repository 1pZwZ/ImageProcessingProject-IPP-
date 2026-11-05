# 🔍 Stage 1: Image Preprocessing (`src/preprocessing/`)

> **Lead Specialist:** Abbas Abdulaziz Al Thunayan (`2240004112`)  
> **Role:** DIP Preprocessing Specialist

---

## 🎯 Module Objectives

This module handles the initial ingestion, spatial filtering, and illumination normalization of raw PlantVillage leaf images before color space segmentation and feature extraction:

1. **Image Ingestion & Standardization:**
   - Load raw leaf images and convert color order from BGR (`cv2`) to standard **RGB**.
   - Resize all images to a uniform **$256 \times 256$ pixels** resolution.
   - Generate stratified dataset splits (**70% Training**, **15% Validation**, **15% Testing**).
2. **Spatial Noise Filtering:**
   - **Gaussian Filtering:** Suppress high-frequency camera sensor noise across leaf surfaces.
   - **Bilateral Filtering:** Perform edge-preserving smoothing so necrotic and chlorotic lesion boundaries remain sharp while background and intra-leaf noise are attenuated.
3. **Illumination & Contrast Normalization (CLAHE):**
   - Apply **Contrast Limited Adaptive Histogram Equalization (CLAHE)** to the luminance channel ($L^*$ in CIELAB or $V$ in HSV) to correct non-uniform lighting and enhance subtle early-stage lesion contrast without amplifying noise.

---

## 🛠️ Planned Components

- `loader.py` — Image loading, RGB validation, $256 \times 256$ resizing, and stratified 70/15/15 split generator.
- `filters.py` — Gaussian filter and bilateral filter implementations with configurable kernel sizes and $\sigma$ parameters.
- `enhancement.py` — CLAHE contrast enhancement on luminance channels (`clipLimit`, `tileGridSize`).

