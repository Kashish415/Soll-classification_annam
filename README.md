# Soil Classification - Annam AI Challenge

## 🔍 Problem Statement
Classify soil images into 4 types: Alluvial, Black, Clay, and Red.

## 📦 Dataset
Provided via Kaggle: `/kaggle/input/soil-classification`

## 🧠 Model
- ResNet18 with partial fine-tuning
- Weighted CrossEntropy Loss (to handle class imbalance)
- Evaluated using minimum F1-score

## 🚀 How to run
Run the final notebook: `notebook.ipynb`

## 📁 Structure
- `notebook.ipynb`: Full training & inference pipeline
- `submission.csv`: Final predictions
