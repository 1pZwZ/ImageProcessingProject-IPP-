# 🖥️ Project Presentation (`presentation/`)

> **Presentation Design Lead:** Mohammed Sameer Alajlan (`2240002025`) — *Evaluation & Visualization Lead*

This directory stores the PowerPoint slide deck (`.pptx` / `.pdf`) and visual assets for Group 2's in-class **ARTI 403 – Image Processing** project presentation and evaluation in **Week 13**.

---

## 📂 Subdirectory Structure

```text
presentation/
├── assets/         # Pipeline diagrams, visual comparisons, and chart exports for slides
└── README.md       # Presentation structure & speaker guide (this file)
```

---

## 🎤 Recommended Slide Deck Flow & Speaker Breakdown

Per the **ARTI 403 Project Guidelines (Section 4)**, all team members must present the project outcomes, discuss their individual contributions, and be prepared to answer questions:

| Part | Speaker | Role | Topics Covered |
| :-: | :--- | :--- | :--- |
| **1** | **Nawaf Rabee Shahbal** | *Team Leader & Pipeline Architect* | Title slide, agricultural problem statement, literature review summary, PlantVillage dataset setup, and end-to-end pipeline overview. |
| **2** | **Abbas Abdulaziz Al Thunayan** | *DIP Preprocessing Specialist* | Image standardization ($256 \times 256$), Gaussian vs. bilateral noise filtering, and CLAHE illumination normalization results. |
| **3** | **Mohammed Nasser Al-Marhoon** | *Color Segmentation Lead* | RGB $\rightarrow$ HSV and CIELAB ($L^*a^*b^*$) color space transformations, $a^*$ channel isolation, K-means ($k=3$) clustering, and Otsu thresholding. |
| **4** | **Faisal Abdullah Alshehri** | *Morphology & Feature Analyst* | Morphological opening/closing mask refinement, lesion boundary extraction, Color Moments, and GLCM texture analysis. |
| **5** | **Saad Abdulaziz Alshehri** | *Machine Learning & CNN Developer* | HOG shape descriptors, multi-modal feature fusion, SVM & Random Forest training, and MobileNetV2 GPU benchmark on Google Colab. |
| **6** | **Mohammed Sameer Alajlan** | *Evaluation & Visualization Lead* | Quantitative comparison tables (Accuracy, F1, ROC-AUC, IoU, Dice, inference latency), confusion matrices, conclusion, and future work. |

