# GliomaSurvivalWeaklySupervised
This project combines weakly-supervised segmentation of glioblastoma tumor regions with Cox survival modeling. It integrates multi-modal MRI data with clinical outcomes to explore the impact of tumor morphology on patient prognosis.

## Objectives
- Apply weakly-supervised segmentation (UNet-based) to BraTS MRI data
- Extract features (tumor volume, region ratio) to be used in survival analysis
- Model overall survival using Cox proportional hazards regression
- Evaluate robustness to missing segmentation labels

## Structure
- `data/`: Includes sample BraTS data and survival metadata
- `segmentation/`: Scripts for training weakly-supervised UNet
- `survival_model/`: Cox regression analysis notebooks
- `results/`: Model outputs, plots, and evaluation metrics

## Future Extensions
- Incorporate semi-supervised learning for segmentation (pseudo-labeling)
- Multiple imputation for missing segmentation data
- Test against real-world clinical EMR if available

- import numpy as np
import matplotlib.pyplot as plt

# Simulate a binary mask as segmentation output
seg_mask = np.zeros((128, 128))
seg_mask[40:90, 50:100] = 1

# Save segmentation mask
np.save("data/mock_segmentation.npy", seg_mask)

# visualize
plt.imshow(seg_mask, cmap="gray")
plt.title("Mock Tumor Mask")
plt.show()



