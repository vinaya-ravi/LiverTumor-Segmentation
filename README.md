# Residual U-Net-Based Liver Tumor Segmentation in CT Imaging

This repository presents a comparative study and implementation of two deep learning architectures **U-Net** and **Residual U-Net (ResU-Net)** for liver tumor segmentation in CT images.

---

## Overview

- **Purpose:**  
  To evaluate and compare the effectiveness of U-Net and ResU-Net models in segmenting liver tumors from CT scans aiming to improve accuracy and reliability for medical diagnostics and treatment planning.

- **Key Features:**  
  - Utilizes a curated subset of the LiTS dataset.
  - Implements robust preprocessing and augmentation techniques.
  - Provides both quantitative and qualitative evaluation of segmentation results.
  - Includes visualization tools for side-by-side result comparison.

---

## Methodology

- **Dataset:**  
  - Based on the LiTS dataset from Kaggle, filtered to include only CT slices with annotated tumor regions.
  - Images and masks are resized to 128×128 pixels and normalized.
  - Data augmentation enhances model robustness.

- **Models:**  
  - **U-Net:** Encoder-decoder architecture with skip connections, effective for biomedical image segmentation.
  - **ResU-Net:** An improved U-Net variant with residual blocks, enabling deeper networks and better feature learning for complex tumor structures.

- **Training Protocol:**  
  - Both models trained on identical data splits with the Adam optimizer and binary cross entropy loss.
  - Early stopping and TensorBoard monitoring are used to prevent overfitting and log progress.

- **Evaluation Metrics:**  
  - Dice Coefficient
  - Intersection over Union (IoU)
  - Structural Similarity Index (SSIM)
  - Precision, Recall, F1-Score

---

## Results Summary

| Model    | Dice   | IoU    | SSIM   | Precision | Recall | F1-Score |
|----------|--------|--------|--------|-----------|--------|----------|
| U-Net    | 0.9465 | 0.9080 | 0.9744 | 0.9680    | 0.9682 | 0.9681   |
| ResU-Net | 0.9621 | 0.9311 | 0.9799 | 0.9777    | 0.9757 | 0.9767   |

- **ResU-Net outperforms U-Net** across all metrics, providing higher segmentation accuracy and sharper boundary detection, especially in small or complex tumor regions.
- Visual comparisons confirm ResU-Net’s improved ability to delineate tumor boundaries and maintain anatomical accuracy.

---

## Applications

- Automated, accurate liver tumor segmentation for medical image analysis.
- Potential integration into clinical workflows for improved diagnosis and treatment planning.

---

## Future Enhancements

- Extension to 3D volumetric and multi-modal segmentation.
- Exploration of attention mechanisms and lightweight models for clinical deployment.