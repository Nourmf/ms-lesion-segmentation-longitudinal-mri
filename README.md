# Longitudinal MS Lesion Segmentation Using Deep Learning

**Author:** Nour Fawaz  
**Course:** VIP 401A  
**Project:** Multiple Sclerosis Lesion Segmentation from Longitudinal FLAIR MRI

## Project Overview

This repository presents a longitudinal MRI pipeline for new multiple sclerosis lesion segmentation using deep learning. The project uses paired baseline and follow-up FLAIR MRI scans to detect newly appearing MS lesions over time.

The work includes two main notebooks:

1. **Baseline MS Lesion Segmentation**
   - Implements the initial lightweight 3D U-Net pipeline.
   - Includes preprocessing, padding, training, inference, visualization, metric evaluation, and baseline hyperparameter grid search.

2. **Refined MS Lesion Segmentation with Post-Processing**
   - Improves the baseline model using residual blocks, attention-gated skip connections, increased feature capacity, and gradient clipping.
   - Adds post-processing using 3D connected-component analysis to reduce isolated false positives and support lesion-level evaluation.
  
## Requirements

The notebooks were developed using:

- Python 3.10
- PyTorch
- NumPy
- SimpleITK
- Matplotlib

The experiments were executed using Google Colab with Google Drive integration.

## Dataset

The experiments were conducted using longitudinal FLAIR MRI scans from the MSSEG longitudinal lesion segmentation challenge dataset.

Each patient case includes:
- baseline FLAIR MRI,
- follow-up FLAIR MRI,
- registered follow-up MRI,
- and ground-truth lesion masks.

The dataset is not included in this repository due to size and access restrictions.

## How to Run

1. Open the notebooks using Google Colab or Jupyter Notebook.
2. Mount Google Drive if using Colab.
3. Update dataset and output paths according to your local environment.
4. Run the preprocessing cells before training or inference.
5. Execute the training and evaluation sections sequentially.

The refined notebook additionally includes:
- residual-attention architecture enhancement,
- post-processing,
- and lesion-level analysis.

## Repository Structure

```text
ms-lesion-segmentation-longitudinal-mri/
│
├── Baseline_MS_Lesion_Segmentation_NourFawaz.ipynb
├── Refined_MS_Lesion_Segmentation_PostProcessing_NourFawaz.ipynb
└── README.md


