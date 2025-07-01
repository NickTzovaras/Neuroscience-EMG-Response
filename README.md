# EMG Response Analysis – Neuroscience & Neural Engineering

This repository contains the lab report for the **"Introduction to Neuroscience and Neural Engineering"** course (NTUA, Academic Year 2024–2025), focusing on the analysis of EMG signals during an object lifting task.

---

## 📘 Project Overview

The objective of this assignment is to:
- Preprocess and analyze EMG data collected from 9 muscle channels.
- Characterize the neuromuscular response related to correct vs. incorrect task performance.
- Apply dimensionality reduction and decomposition techniques.
- Evaluate classification performance for decoding behavioral outcomes.

---

## 📁 Dataset Description

### EMG Data
- Stored in the variable `processed_emg`.
- A cell array, where each **cell = one trial**.
- Each trial is a matrix of shape **N_timepoints × 9**, where 9 = muscle channels.

### Behavioral Data
Stored in `.csv` files with trial metadata:
- `response`: 1 = correct, 0 = incorrect.
- `reaction time`: in ms.
- `weight`: object weight.
- `direction`: movement direction.

**Target variable for classification**: `response`

---

## 🧪 Methods

### ✅ A. Dimensionality Reduction
- Applied **Principal Component Analysis (PCA)** to normalized EMG data.
- Found that **107 principal components** explain 90% of the variance.

### ✅ B. Visualization
- Plotted the first two **PCA coefficients** and their **trial-averaged scores**.
- Analysis revealed:
  - Clear activation patterns differentiating correct vs. incorrect responses.
  - Muscles 1 and 2 contributed most to class separability.

### ✅ C. Source Separation
- Applied **Independent Component Analysis (ICA)**.
- Explored differences between PCA and ICA for capturing task-relevant variance.

### ✅ D. Feature Extraction & Classification
- Extracted temporal and spatial features.
- Trained classifiers to decode the `response` label.
- Evaluated classification performance using accuracy metrics.

---

## 🧰 Technologies

- Python (NumPy, SciPy, pandas, scikit-learn)
- Jupyter Notebook / Google Colab
- EMG signal processing methods
- Dimensionality reduction and machine learning

---

## 📊 Results

- PCA uncovered low-dimensional structure explaining most signal variance.
- Muscle-specific activation patterns were observed between correct/incorrect trials.
- Classification performance indicated discriminative patterns embedded in the EMG features.

---

## 📌 Credits

**Authors**: Petros Kotoulas, Nikolaos-Andreas Tzovaras  
**Institution**: NTUA – MSc in Translational Engineering in Health and Medicine  
**Course**: Introduction to Neuroscience and Neural Engineering  
**Year**: 2024–2025

---
