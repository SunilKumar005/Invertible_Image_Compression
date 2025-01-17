# Invertible Image Compression

## Overview
Invertible Image Compression (IIC) is a deep learning-based approach designed for efficient image compression while ensuring lossless or near-lossless reconstruction. The model leverages invertible neural networks, discrete wavelet transforms (DWT), and high-pass component estimators to retain essential image details, achieving high fidelity in image restoration.

This repository provides a comprehensive pipeline, from dataset preparation to model training and evaluation.

---

## Features
- **Lossless Compression:** Utilizes invertible networks for accurate reconstruction.
- **Wavelet Decomposition:** Decomposes images into low and high-frequency components for better compression.
- **Customizable Modules:** Includes IIG (Invertible Image Generation) modules for flexible adaptation.
- **Automated Dataset Handling:** Seamless integration with Kaggle datasets for quick setup.
- **Comprehensive Evaluation Metrics:** Includes tools for evaluating reconstruction quality and compression efficiency.

---

## Prerequisites
- Python 3.8 or higher
- Kaggle account with an API key (`kaggle.json`)
- Libraries: PyTorch, NumPy, OpenCV, Scikit-image, Matplotlib, and others specified in `requirements.txt`.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/SunilKumar005/Invertible_Image_Compression.git
   cd Invertible_Image_Compression
   ```
2. Set up Kaggle API key:
   ```bash
   !mkdir ~/.kaggle
   !mv kaggle.json ~/.kaggle/
   chmod 600 ~/.kaggle/kaggle.json
   ```

---

## Dataset Preparation
1. **Download Dataset from Kaggle:**
   Use the following command to fetch the dataset:
   ```bash
   !kaggle datasets download -d joe1995/div2k-dataset
   ```

2. **Extract Dataset:**
   Unzip the downloaded dataset for training and evaluation:
   ```bash
   !unzip div2k-dataset.zip -d data/
   ```

---

## Model Architecture
1. **IIG Module:** A core component for invertible image transformations, ensuring lossless compression and decompression.
2. **Wavelet Decomposition:** Utilizes discrete wavelet transforms to split images into multiple frequency bands.
3. **High-Pass Estimators:** Refines details in high-frequency bands for accurate restoration.
4. **Training Pipeline:** Optimized for color consistency and minimal reconstruction loss.

---

## Results
- **Compression Ratio:** Achieved efficient compression with minimal data loss.
- **Reconstruction Quality:** High PSNR and SSIM scores across datasets.
- **Color Accuracy:** Maintains color fidelity across RGB channels.
