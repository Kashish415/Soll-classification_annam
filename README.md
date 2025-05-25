# Soil Image Classification (Annam AI Challenge - Part 1)

This repository contains my solution for **Part 1** of the Soil Image Classification Challenge hosted on Kaggle as part of the Annam.ai competition at IIT Ropar. The task was to classify soil images into one of four types: **Alluvial, Black, Clay, or Red**.

## Project Overview

- **Problem Type**: Multi-class image classification
- **Classes**: Alluvial, Black, Clay, Red
- **Evaluation Metric**: Minimum F1-score across all classes 

## Dataset

- Images are provided in `train/` and `test/` directories.
- A `train_labels.csv` file maps each training image to its corresponding soil type.
- The `test_ids.csv` file contains the IDs of images to be predicted.

- **Backbone**: Partially fine-tuned `ResNet18` with a custom classification head and dropout.
- **Data Augmentation**: Random horizontal flips and slight rotations.
- **Loss Function**: Weighted CrossEntropyLoss to handle class imbalance.
- **Optimizer**: Adam with layer-wise learning rates
- **Evaluation**: Macro F1-score computed on a stratified validation split

## Highlights

- Clean and modular PyTorch implementation
- Used weighted loss to handle class imbalance
- Trained using stratified 80-20 train-validation split
- Saved the best model based on validation F1-score
- Generated a final `submission.csv` using the best model
- Included final evaluation code to compute per-class and minimum F1 on validation set

  ## Result

- Achieved **minimum per-class F1-score of 0.9655 on validation set
- Generated submission for Kaggle as per competition rules

