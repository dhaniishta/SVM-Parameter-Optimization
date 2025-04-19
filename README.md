# SVM Parameter Optimization - Letter Recognition Dataset 

## Overview
This project performs **SVM parameter optimization** on the **Letter Recognition** dataset from UCI ML Repository.  
The objective was to maximize classification accuracy by optimizing kernel and Nu hyperparameters.

---

## Dataset Details
- **Dataset**: [Letter Recognition Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/letter-recognition/letter-recognition.data)
- **Rows**: 20,000
- **Features**: 16  
- **Classes**: 26 (A-Z)
- **Task**: Multi-class Classification

---

## Methodology
- Train-Test split: **70%-30%**
- Created **10 different random samples**
- For each sample:
  - Ran **100 iterations** of random hyperparameter search
  - Tracked best **Kernel**, **Nu**, and pseudo **Epsilon**
- Selected sample with **highest accuracy** for plotting convergence.

---

## Table 1: Comparative Performance of Optimized-SVM with Different Samples

| Sample # | Best Accuracy | Best SVM Parameters |
|:--------:|:-------------:|:-------------------:|
| S1 | 0.932667 | {'Kernel': 'rbf', 'Nu': 0.134, 'Epsilon': 0.25} |
| S2 | 0.937667 | {'Kernel': 'rbf', 'Nu': 0.102, 'Epsilon': 0.36} |
| S3 | 0.938667 | {'Kernel': 'rbf', 'Nu': 0.109, 'Epsilon': 0.491} |
| S4 | 0.934000 | {'Kernel': 'rbf', 'Nu': 0.128, 'Epsilon': 0.072} |
| S5 | 0.943167 | {'Kernel': 'rbf', 'Nu': 0.103, 'Epsilon': 0.344} |
| S6 | 0.919833 | {'Kernel': 'rbf', 'Nu': 0.148, 'Epsilon': 0.038} |
| S7 | 0.908500 | {'Kernel': 'poly', 'Nu': 0.105, 'Epsilon': 0.494} |
| S8 | 0.933333 | {'Kernel': 'rbf', 'Nu': 0.133, 'Epsilon': 0.494} |
| S9 | **0.945500** | {'Kernel': 'rbf', 'Nu': 0.103, 'Epsilon': 0.248} |
| S10 | 0.895000 | {'Kernel': 'poly', 'Nu': 0.126, 'Epsilon': 0.303} |

---

## Convergence Graph

Fitness vs Iteration for best performing sample (Sample 9).

![Convergence Graph](https://github.com/dhaniishta/SVM-Parameter-Optimization/blob/main/graph.jpeg?raw=true)
