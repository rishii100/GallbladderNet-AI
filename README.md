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

![image](https://github.com/user-attachments/assets/7657f99d-a7ec-4851-8368-ddb7bb358216)


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

## 🖼️ Result & Visualizations:

### 📉 Accuracy Curve:
![image](https://github.com/user-attachments/assets/641f6cea-2969-4cf8-9c33-e383e4a4362d)


### 📌 Confusion Matrix
![image](https://github.com/user-attachments/assets/eda28759-a53b-44ad-9698-34c7ebc71bd5)


### 📈 ROC Curve
![image](https://github.com/user-attachments/assets/04561aa9-d10d-45ed-8329-4e119558ebb3)


### 🔄 PR Curve
![image](https://github.com/user-attachments/assets/86469a9b-c8b2-44d0-9c48-ea55a4ac814c)


### ❌ Misclassified Samples
![image](https://github.com/user-attachments/assets/f614dd8e-ef5a-47dc-a854-8d64ede20625)


---
---
### 📜 License
Licensed under the [Apache License 2.0](LICENSE)
