# 🧩 Source Code (`src/`) — Modular DIP & ML Pipeline

This directory contains the modular Python package implementing the **Safe Gardens** Digital Image Processing (DIP) and Machine Learning pipeline.

---

## 🏗️ Package Architecture & Module Ownership

```text
src/
├── __init__.py
├── preprocessing/      # Stage 1: Resizing, Gaussian/Bilateral filtering, CLAHE
├── segmentation/       # Stage 2: RGB → HSV/CIELAB conversion, K-means (k=3), Otsu
├── morphology/         # Stage 3: Morphological opening/closing, binary mask refinement
├── features/           # Stage 4: Color moments, GLCM texture, and HOG descriptors
├── models/             # Stage 5: SVM, Random Forest, and MobileNetV2 CNN baseline
└── evaluation/         # Stage 6: Classification/segmentation metrics & visualizations
```

| Subpackage | Pipeline Stage | Lead Developer | Key Algorithms & Techniques |
| :--- | :--- | :--- | :--- |
| [`preprocessing/`](./preprocessing/) | **1. Image Preprocessing** | **Abbas Abdulaziz Al Thunayan** | Stratified data splitting (70/15/15), $256 \times 256$ resizing, Gaussian smoothing, edge-preserving bilateral filtering, CLAHE illumination normalization. |
| [`segmentation/`](./segmentation/) | **2. Color Space Segmentation** | **Mohammed Nasser Al-Marhoon** | RGB $\rightarrow$ HSV and CIELAB ($L^*a^*b^*$) transformation, $a^*$ & Hue/Saturation channel isolation, K-means clustering ($k=3$), Otsu thresholding. |
| [`morphology/`](./morphology/) | **3. Morphological Processing** | **Faisal Abdullah Alshehri** | Structuring element design, morphological opening (noise removal) and closing (lesion gap filling), connected components, lesion contour extraction. |
| [`features/`](./features/) | **4. Multi-Modal Feature Extraction** | **Faisal Abdullah Alshehri** & **Saad Abdulaziz Alshehri** | Color moments (mean, std, skewness), GLCM texture features (contrast, correlation, energy, homogeneity), HOG gradient/shape descriptors. |
| [`models/`](./models/) | **5. Classification & CNN Benchmark** | **Saad Abdulaziz Alshehri** | Feature scaling, Support Vector Machine (SVM), Random Forest classifier, and fine-tuned MobileNetV2 deep learning benchmark. |
| [`evaluation/`](./evaluation/) | **6. Evaluation & Visualization** | **Mohammed Sameer Alajlan** | Accuracy, Precision, Recall, F1-Score, ROC-AUC, Confusion Matrix, Segmentation IoU & Dice coefficient, inference latency (ms/image) benchmarks. |

---

## 📐 Coding Conventions

- **Color Channel Convention:** All public functions inside `src/` operate on **RGB** `numpy.ndarray` images of shape `(256, 256, 3)` with `uint8` range `[0, 255]`, unless explicitly specified in the function docstring.
- **Documentation:** Every module and function should include clear docstrings describing input parameters, return types, and the underlying Digital Image Processing mathematical concept.

