# Glioblastoma Semi-Supervised Segmentation and Survival Prediction

This project explores semi-supervised learning for glioblastoma (GBM) MRI segmentation under weak labeling conditions, and extends to survival modeling based on extracted radiomics features.

Due to the scarcity of fully-annotated BraTS data, we emulate a weak labeling setting and develop a prototype pipeline using PyTorch and PyRadiomics. This project aims to bridge weakly-supervised imaging tasks with downstream clinical outcome modeling.

## Project Structure
- `data/`: Simulated small-scale 3D MRI data.
- `scripts/`: Code for data preparation, segmentation, feature extraction, and survival analysis.
- `results/`: Saved outputs including segmentation visualizations and survival curves.

## Main Steps
1. Simulate and load small MRI datasets.
2. Generate weak segmentation annotations.
3. Train a semi-supervised segmentation model.
4. Extract radiomics features.
5. Perform Cox regression for survival prediction.
6. Assess robustness via missing data simulation and imputation.
7. Summarize findings and visualizations.

## Requirements
- Python 3.8+
- Key libraries: PyTorch, SimpleITK, PyRadiomics, scikit-learn, matplotlib
