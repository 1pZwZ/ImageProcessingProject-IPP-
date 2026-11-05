# 📝 IEEE Conference Research Paper (`paper/`)

> **Compilation Lead:** Nawaf Rabee Shahbal (`2240009025`) — *Team Leader*  
> **Template Standard:** [IEEE Manuscript Templates for Conference Proceedings](https://www.ieee.org/conferences/publishing/templates.html)

This directory contains the drafts, high-resolution figures, and final Week 13 submission files for our **ARTI 403 – Image Processing** research paper:
> **"Safe Gardens: Automated Detection and Classification of Plant Leaf Diseases Using Color Space Segmentation, Texture Feature Analysis, and Deep Learning"**

---

## 📂 Subdirectory Structure

```text
paper/
├── drafts/         # Word (.docx) / LaTeX manuscript drafts, final PDF, and similarity report
├── figures/        # Publication-ready figures and architecture diagrams for the manuscript
└── README.md       # Paper structure & submission checklist (this file)
```

---

## 📑 Required Paper Structure (ARTI 403 Guidelines — Section 5)

Our manuscript follows the seven-section structure specified in [`../Documents/ARTI 403 - Project Guidelines.pdf`](../Documents/ARTI%20403%20-%20Project%20Guidelines.pdf):

### I. Introduction
- Introduce the real-world problem of crop yield loss (20%–40% annually) caused by fungal, bacterial, and viral plant leaf diseases.
- Explain the importance and relevance of automated diagnosis in the context of **Digital Image Processing (DIP)**.
- Provide a clear overview of the **Safe Gardens** pipeline and overall approach.

### II. Project Goals and Objectives
- State the main goal of the project.
- Define specific, measurable objectives across preprocessing, color space segmentation, multi-modal feature extraction, and classification.
- Identify expected performance and evaluation criteria (Classical DIP + ML target F1 $\ge 94\%$; MobileNetV2 CNN baseline target F1 $\ge 98\%$).

### III. Related Work (Literature Review)
- Review relevant research articles from reputable academic sources (Mohanty et al. [1], Singh & Misra [2], Ramesh et al. [3]).
- Summarize existing DIP and deep learning techniques, identify limitations/gaps, and explain how **Safe Gardens** builds upon and compares them.

### IV. Data Acquisition and Preprocessing
- Describe the **PlantVillage Dataset** (54,306 RGB images, 38 classes, 14 crop species, $256 \times 256$ resolution, 70/15/15 stratified split) and provide dataset links.
- Detail the DIP preprocessing steps: resizing, **Gaussian filtering**, **bilateral filtering**, and **CLAHE** illumination normalization.

### V. Image Processing and Model Development
- Detail the color space transformation (**RGB $\rightarrow$ HSV** and **CIELAB $L^*a^*b^*$**).
- Explain lesion segmentation via **K-means clustering ($k=3$)** and **Otsu thresholding**, followed by **morphological opening and closing**.
- Describe multi-modal feature extraction (**Color Moments**, **GLCM texture descriptors**, and **HOG shape features**).
- Detail the classical classifiers (**SVM**, **Random Forest**) and the GPU-accelerated **MobileNetV2** CNN architecture and training protocol.

### VI. Results, Discussion, and Visualization
- Present experimental results using clear quantitative tables and multi-stage visual comparisons.
- Evaluate models using **Accuracy, Precision, Recall, F1-Score, ROC-AUC**, **Confusion Matrices**, segmentation **IoU & Dice**, and **inference speed (ms/image)**.
- Discuss findings, compare classical DIP vs. CNN trade-offs, and analyze limitations.

### VII. Conclusion and Future Work
- Summarize main objectives, methodology, and quantitative findings.
- Highlight key contributions and real-world precision agriculture applications (e.g., mobile field diagnostics).
- Provide recommendations for future improvements (e.g., in-field background clutter robustness, lightweight edge deployment).

---

## ✅ Week 13 Paper Submission Checklist

- [ ] Manuscript formatted strictly using the **IEEE Conference Proceedings Template** (with template source cited in footnotes).
- [ ] Project title and all 6 Group 2 team members clearly identified on the title page.
- [ ] Final paper exported in **Word (`.docx`)** format.
- [ ] Final paper exported in **PDF (`.pdf`)** format.
- [ ] **Plagiarism / Similarity Report** attached inside `paper/drafts/`.

