# 🧬 Stage 3: Morphological Post-Processing (`src/morphology/`)

> **Lead Specialist:** Faisal Abdullah Alshehri (`2240001737`)  
> **Role:** Morphology & Feature Analyst

---

## 🎯 Module Objectives

Raw segmentation masks from K-means clustering or Otsu thresholding often contain isolated noise pixels (spurious false positives) or small holes inside necrotic spots. This module refines segmented masks using mathematical morphology:

1. **Morphological Opening ($\circ$):**
   - Erosion followed by dilation using elliptical/disk structuring elements to eliminate small isolated background specks and leaf-vein artifacts.
2. **Morphological Closing ($\bullet$):**
   - Dilation followed by erosion to bridge narrow gaps and fill internal holes within contiguous disease lesions.
3. **Lesion Boundary & ROI Extraction:**
   - Extract clean binary lesion masks, lesion contours/perimeters, and masked RGB/CIELAB Regions of Interest (ROIs) for downstream feature extraction.

---

## 🛠️ Planned Components

- `operations.py` — Configurable morphological erosion, dilation, opening, closing, and hole-filling routines.
- `mask_refinement.py` — Connected-component filtering, lesion boundary extraction, and ROI masking utilities.

