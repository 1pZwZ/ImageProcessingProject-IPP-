# 🤝 Contributing Guide — Safe Gardens (Group 2)

Welcome to the **Safe Gardens (ARTI 403 – Group 2)** repository! This document outlines our team's workflow, folder ownership, naming conventions, and coding standards so we can collaborate cleanly without merge conflicts.

---

## 👥 Module Ownership by Team Member

Each team member is the primary owner of their respective pipeline directory in [`src/`](./src/) and corresponding notebook in [`notebooks/`](./notebooks/):

| Team Member | Role | Owned Directories / Files |
| :--- | :--- | :--- |
| **Nawaf Rabee Shahbal** *(Leader)* | Project Lead & Pipeline Architect | [`src/`](./src/) integration, [`data/splits/`](./data/splits/), [`paper/`](./paper/) |
| **Abbas Abdulaziz Al Thunayan** | DIP Preprocessing Specialist | [`src/preprocessing/`](./src/preprocessing/), `notebooks/01_preprocessing.ipynb` |
| **Mohammed Nasser Al-Marhoon** | Color Segmentation Lead | [`src/segmentation/`](./src/segmentation/), `notebooks/02_color_segmentation.ipynb` |
| **Faisal Abdullah Alshehri** | Morphology & Feature Analyst | [`src/morphology/`](./src/morphology/), [`src/features/`](./src/features/), `notebooks/03_morphology_and_features.ipynb` |
| **Saad Abdulaziz Alshehri** | ML & CNN Developer | [`src/features/`](./src/features/) (HOG), [`src/models/`](./src/models/), `notebooks/04_classical_ml.ipynb`, `notebooks/05_cnn_mobilenetv2.ipynb` |
| **Mohammed Sameer Alajlan** | Evaluation & Visualization Lead | [`src/evaluation/`](./src/evaluation/), [`results/`](./results/), [`presentation/`](./presentation/), `notebooks/06_evaluation_and_visualization.ipynb` |

---

## 🌿 Git Branching Workflow

1. **Never push untested or broken code directly to `main`.**
2. Create a descriptive feature branch for your task:
   - `feat/preprocessing-clahe` *(Abbas)*
   - `feat/segmentation-kmeans-otsu` *(Mohammed N.)*
   - `feat/morphology-glcm` *(Faisal)*
   - `feat/models-svm-rf-cnn` *(Saad)*
   - `feat/evaluation-metrics-plots` *(Mohammed S.)*
   - `docs/ieee-paper-draft` *(Nawaf)*
3. Pull the latest changes from `main` before opening a Pull Request (PR):
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feat/your-branch-name
   ```

---

## 📝 Commit Message Conventions

Use clear, concise commit messages prefixed with a category tag:
- `feat:` Adding a new image processing function, feature extractor, or model
- `fix:` Fixing a bug in filtering, segmentation, or metric calculation
- `docs:` Updating `README.md`, docstrings, or paper files
- `exp:` Adding experimental results, plots, or notebook runs
- `refactor:` Cleaning up or restructuring existing code

**Examples:**
- `feat(preprocessing): implement bilateral filter and CLAHE normalization`
- `feat(segmentation): add CIELAB a* channel K-means (k=3) clustering`
- `docs(paper): add Section III related work draft`

---

## 🧹 Code & Notebook Guidelines

1. **Standardized Image Format:**
   - All pipeline functions should expect or output images resized to **$256 \times 256$**.
   - Clearly document in every function docstring whether an image array is expected in **RGB** or **BGR** (remember `cv2.imread` loads in BGR by default; convert via `cv2.cvtColor(img, cv2.COLOR_BGR2RGB)`).
2. **Docstrings & Comments:**
   - As required by the **ARTI 403 Project Guidelines**, all Python functions and Jupyter Notebooks must be well-organized, properly commented, and easy to understand.
3. **Do Not Commit Bulk Datasets or Large Model Checkpoints:**
   - Keep the full PlantVillage dataset inside `data/raw/` (which is automatically ignored by `.gitignore`).
   - Only commit lightweight sample images to `data/samples/` and final plots/tables to `results/figures/` and `results/metrics/`.

