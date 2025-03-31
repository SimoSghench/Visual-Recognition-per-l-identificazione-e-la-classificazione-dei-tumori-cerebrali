# Visual Recognition for Brain Tumor Classification

## Overview

This project implements a visual recognition system aimed at identifying and classifying two types of brain tumors – Glioblastoma (GBM) and Metastases (MET) – using MRI images. The approach leverages state-of-the-art deep learning techniques with pre-trained CNN architectures (e.g., ResNet, EfficientNet, VGG) and the Fuse-Med-ML framework to efficiently process and analyze medical imaging data.

## Motivation

Early and accurate tumor classification can be a vital support tool in the diagnostic process. This project explores the potential of deep learning in medical imaging by comparing various models, implementing a two-level classification strategy (using both CNNs and ensemble methods like Random Forest and MLP), and analyzing performance through multiple evaluation metrics.
  
## Datasets

Two datasets are used:
- **VOL Dataset:** Contains approximately 1412 post-contrast volumetric MRI images organized into training, validation, and testing subsets.
- **MULTI Dataset:** Composed of 1692 multimodal MRI images (across 6 different MRI sequences) aggregated into 282 samples, each containing images of ADC, DWI, FLAIR, GRE, T1W, and T1W+MDC categories.

## Methodology

1. **Data Preprocessing:**  
   - Image resizing (typically to 224x224 pixels)  
   - Normalization (comparing MNIST and ResNet/VGG normalization standards)  
   - Conversion to tensors for PyTorch compatibility

2. **Modeling:**  
   - Utilization of pre-trained CNNs (ResNet variants, VGG, EfficientNet)  
   - Integration with Fuse-Med-ML for handling multimodal data  
   - Experimentation with various architectures to find the best model performance

3. **Training & Evaluation:**  
   - Hyperparameter tuning (batch size, epochs, learning rate, weight decay, optimizer, and loss function)  
   - Use of evaluation metrics such as Accuracy, Precision, Recall, F1-Score, ROC curves, and AUC  
   - Comparison of single image predictions (per MRI sequence) and ensemble-level predictions using Random Forest and MLP
