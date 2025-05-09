# GallbladderNet-AI

A deep learning ensemble approach using transfer learning to detect gallbladder cancer from ultrasound images. This project combines multiple pretrained CNN architectures for improved accuracy, calibration, and robustness in clinical diagnosis.

---

## 🧪 Overview

This project implements a multi-model deep learning ensemble to classify gallbladder ultrasound images into **Normal**, **Benign**, and **Malignant** categories. It uses **transfer learning**, **soft voting ensembles**, and performance visualizations such as **ROC**, **PR**, and **Calibration Curves** to support decision-making in medical diagnosis.

---

## 📁 Dataset

- **Source:** [Kaggle – Gallbladder Ultrasound Cancer Dataset](https://www.kaggle.com/datasets/aneerbansaha/gallbladder-cancer)
- **Classes:** Normal, Benign, Malignant
- **Format:** Ultrasound images
- **Preprocessing:** 
  - Resizing, normalization
  - Data augmentation (random flip, jitter, rotation)
  - Class balancing using sampling and weighted loss

---

## 🏗️ Model Architecture

- **Base Models:**
  - VGG19
  - ResNet50
  - EfficientNetB3
- **Modifications:**
  - Removed top layers
  - Added custom dense layers with dropout
- **Fusion Technique:** 
  - Feature-level fusion and soft-voting ensemble

---

## ⚙️ Training Details

- Optimizer: `Adam`
- Loss: `Categorical Crossentropy` with class weights
- Regularization: Dropout, Label Smoothing
- Scheduler: `ReduceLROnPlateau`
- Augmentations: MixUp, Random Rotation, Flip
- Epochs: 30 (with Early Stopping)

---

## 📊 Evaluation Metrics

| Metric     | Value  |
|------------|--------|
| Accuracy   | 85.71% |
| Precision  | 0.86   |
| Recall     | 0.85   |
| F1-Score   | 0.85   |
| AUC-ROC    | 0.92   |

---

## 🖼️ Visualizations

### 📌 Confusion Matrix
- Displays predicted vs. actual classes for model performance overview.

### 📈 ROC Curve
- Plots true positive rate vs. false positive rate for each class.

### 📊 Precision-Recall (PR) Curve
- Highlights model performance in handling class imbalance.

### 🎯 Calibration Curve
- Assesses how well the model's predicted probabilities reflect true confidence.

### ❌ Misclassified Samples
- Visual examples of incorrect predictions with true vs. predicted labels.

---
### 📜 License
Licensed under the [Apache License 2.0](LICENSE)
