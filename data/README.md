# 🍃 Dataset Directory — PlantVillage

This directory houses the dataset files, stratified split manifests, and sample leaf images used in the **Safe Gardens** pipeline.

---

## 📊 Dataset Overview

| Property | Details |
| :--- | :--- |
| **Dataset Name** | **PlantVillage Dataset** (Hughes & Salathé, Penn State University / EPFL) |
| **Total Volume** | ~54,306 RGB leaf images |
| **Classes** | 38 crop-disease categories spanning 14 crop species (e.g., Tomato, Potato, Corn, Apple, Grape — both healthy and diseased foliage) |
| **Image Format & Resolution** | RGB color images (`JPG` / `PNG`), standardized to **$256 \times 256$ pixels** |
| **Partitioning Protocol** | Stratified split: **70% Training** / **15% Validation** / **15% Testing** |
| **Official Download Links** | • [Mendeley Data Repository](https://data.mendeley.com/datasets/tywbtsjrjv/1)<br>• [Kaggle Dataset Mirror](https://www.kaggle.com/datasets/emmarex/plantdisease) |
| **Access Date** | October 17, 2026 |

---

## 📂 Subdirectory Layout

```text
data/
├── raw/            # Place downloaded PlantVillage class folders here (ignored by Git)
├── processed/      # Cached 256×256 filtered & CLAHE-enhanced images (ignored by Git)
├── splits/         # Stratified CSV/JSON manifests (train.csv, val.csv, test.csv)
├── samples/        # Small curated subset of leaf images committed to Git for quick testing
└── README.md       # Dataset documentation (this file)
```

---

## ⚙️ Setup Instructions

1. Download the **PlantVillage Dataset** from [Mendeley Data](https://data.mendeley.com/datasets/tywbtsjrjv/1) or [Kaggle](https://www.kaggle.com/datasets/emmarex/plantdisease).
2. Extract the class folders into `data/raw/` so the structure looks like:
   ```text
   data/raw/
   ├── Apple___Apple_scab/
   ├── Apple___Black_rot/
   ├── Apple___Cedar_apple_rust/
   ├── Apple___healthy/
   ├── Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot/
   ├── ...
   └── Tomato___Tomato_Yellow_Leaf_Curl_Virus/
   ```
3. Run the dataset splitting utility (in [`../src/preprocessing/`](../src/preprocessing/)) to generate the reproducible **70% / 15% / 15% stratified split** CSV files inside `data/splits/`.

> **Note:** Bulk image files inside `data/raw/` and `data/processed/` are excluded via [`.gitignore`](../.gitignore) to keep the Git repository lightweight. Only commit small sample images inside `data/samples/` and split manifest files inside `data/splits/`.

