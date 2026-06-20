# Brain Tumor Segmentation using Attention U-Net and Standard U-Net

This repository contains a deep learning project for **brain tumor segmentation from multi-modal MRI scans** using the **BraTS 2020 H5 slice-format dataset**. The project trains and evaluates an Attention U-Net model and compares it with a Standard U-Net baseline.

## Project Overview

- **Task:** Semantic segmentation of brain tumor regions from MRI scans
- **Dataset:** BraTS 2020 Training Data in `.h5` slice format
- **Input modalities:** FLAIR, T1, T1CE, and T2
- **Output:** Multi-channel tumor segmentation mask
- **Main model:** Attention U-Net
- **Baseline model:** Standard U-Net
- **Framework:** TensorFlow / Keras

## Repository Structure

```text
brain-tumor-segmentation-github-ready/
│
├── notebooks/
│   └── brain_tumor_segmentation_attention_unet_standard_unet.ipynb
│
├── docs/
│   └── project_documentation.docx
│
├── results/
│   ├── *.png        # training curves, overlays, qualitative results
│   ├── *.json       # testing metrics and comparison results
│   ├── *.csv        # training logs
│   └── *.txt        # project summaries
│
├── model_weights/
│   └── place trained model files here, for example .keras or .h5 files
│
├── requirements.txt
├── .gitignore
├── .gitattributes
└── README.md
```

## Results Summary

The project includes training curves, segmentation overlays, model comparison files, and testing summaries in the `results/` folder.

Example reported test results:

| Model | Loss | Metric |
|---|---:|---:|
| Attention U-Net | 0.2423175424337387 | 0.7663708925247192 |
| Loaded Attention U-Net | 0.2423175424337387 | 0.7663708925247192 |
| Standard U-Net | 0.21949324011802673 | 0.7881420254707336 |

> Note: In the notebook, the displayed `compile_metrics` value corresponds to the compiled segmentation metric used during testing.

## How to Run

1. Clone this repository.
2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Download/add the BraTS 2020 dataset in H5 format.
4. Open the notebook from the `notebooks/` folder.
5. Update the dataset path if required.
6. Run the notebook cells for training, evaluation, saving/loading models, and result visualization.

## Model Weights

Large trained model files such as `.keras`, `.h5`, `.pt`, or `.pth` should be stored using **Git LFS**. Place trained weights in the `model_weights/` folder.

Example expected files:

```text
model_weights/attention_unet_best_model.keras
model_weights/attention_unet_final_model.keras
model_weights/attention_unet_weights.weights.h5
model_weights/standard_unet_best_model.keras
model_weights/standard_unet_final_model.keras
model_weights/standard_unet_weights.weights.h5
```

## Important Notes

- The dataset itself is not included in this repository because medical datasets are usually large and may have access restrictions.
- The included Word document explains the project methodology, model architecture, results, and discussion.
- The `results/` folder contains visual outputs and quantitative evaluation files.

## Author

Muhammad Usama Anwar
