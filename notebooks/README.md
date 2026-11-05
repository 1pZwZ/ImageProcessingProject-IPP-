# 📓 Jupyter Notebooks — Safe Gardens Pipeline

This directory contains the interactive Jupyter Notebooks (`.ipynb`) for step-by-step experimentation, visual verification, and end-to-end execution of the **Safe Gardens** Digital Image Processing and Machine Learning pipeline.

---

## 🗂️ Planned Notebook Sequence

To keep our work modular and aligned with our proposal's responsibilities, notebooks follow a numbered sequence:

| Notebook File | Pipeline Stage | Primary Owner(s) | Description |
| :--- | :--- | :--- | :--- |
| `00_complete_pipeline_master.ipynb` | **End-to-End Pipeline** | **Nawaf Rabee Shahbal** *(Team Leader)* | Master notebook integrating all stages from image ingestion to final classification for Week 13 submission. |
| `01_preprocessing.ipynb` | **Stage 1: Preprocessing** | **Abbas Abdulaziz Al Thunayan** | Image ingestion, $256 \times 256$ resizing, Gaussian vs. bilateral filtering comparison, and CLAHE illumination normalization. |
| `02_color_segmentation.ipynb` | **Stage 2: Color Segmentation** | **Mohammed Nasser Al-Marhoon** | RGB $\rightarrow$ HSV and CIELAB ($L^*a^*b^*$) channel visualizations, $a^*$ channel analysis, K-means clustering ($k=3$), and Otsu thresholding. |
| `03_morphology_and_features.ipynb` | **Stage 3 & 4: Morphology & Texture/Color Features** | **Faisal Abdullah Alshehri** | Morphological opening/closing, lesion boundary extraction, Color Moments, and GLCM texture descriptors (contrast, correlation, energy, homogeneity). |
| `04_classical_ml_classification.ipynb` | **Stage 4 & 5A: HOG & Classical Classifiers** | **Saad Abdulaziz Alshehri** | HOG shape descriptor extraction, multi-modal feature vector fusion, and training/tuning of **SVM** and **Random Forest** models. |
| `05_cnn_mobilenetv2_colab.ipynb` | **Stage 5B: Deep Learning Baseline** | **Saad Abdulaziz Alshehri** | GPU-accelerated fine-tuning of **MobileNetV2** on Google Colab for baseline comparison against classical DIP methods. |
| `06_evaluation_and_visualization.ipynb` | **Stage 6: Evaluation & Visualizations** | **Mohammed Sameer Alajlan** | Comprehensive metrics (Accuracy, Precision, Recall, F1, ROC-AUC, IoU, Dice), confusion matrices, runtime benchmarks, and paper-ready figures. |

---

## 💡 Best Practices for Notebooks

1. **Import Reusable Functions from `src/`:**
   Add the project root to `sys.path` at the top of each notebook so you can import shared modules from [`../src/`](../src/):
   ```python
   import sys
   from pathlib import Path
   sys.path.append(str(Path.cwd().parent))
   ```
2. **Clear Temporary Outputs Before Committing (or Keep Final Demo Outputs Clean):**
   Ensure all cells run top-to-bottom without errors (`Kernel -> Restart & Run All`) before opening a Pull Request.
3. **Save Generated Plots to `results/figures/`:**
   Export high-resolution figures (`dpi=300`) directly to [`../results/figures/`](../results/figures/) for inclusion in the IEEE research paper and presentation slides.

