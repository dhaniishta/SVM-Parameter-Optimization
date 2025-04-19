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
| S1 | 0.879 | {‘Kernel’: ‘rbf’, ‘Nu’: 0.431, ‘Epsilon’: 0.123} |
| S2 | 0.867 | {‘Kernel’: ‘linear’, ‘Nu’: 0.512, ‘Epsilon’: 0.214} |
| S3 | 0.872 | {‘Kernel’: ‘rbf’, ‘Nu’: 0.405, ‘Epsilon’: 0.177} |
| S4 | **0.881** | {‘Kernel’: ‘rbf’, ‘Nu’: 0.387, ‘Epsilon’: 0.301} |
| S5 | 0.863 | {‘Kernel’: ‘poly’, ‘Nu’: 0.532, ‘Epsilon’: 0.239} |
| S6 | 0.870 | {‘Kernel’: ‘linear’, ‘Nu’: 0.678, ‘Epsilon’: 0.453} |
| S7 | 0.875 | {‘Kernel’: ‘rbf’, ‘Nu’: 0.490, ‘Epsilon’: 0.128} |
| S8 | 0.878 | {‘Kernel’: ‘rbf’, ‘Nu’: 0.419, ‘Epsilon’: 0.185} |
| S9 | 0.869 | {‘Kernel’: ‘linear’, ‘Nu’: 0.606, ‘Epsilon’: 0.341} |
| S10 | 0.866 | {‘Kernel’: ‘poly’, ‘Nu’: 0.520, ‘Epsilon’: 0.217} |

---

## Convergence Graph

Fitness vs Iteration for best performing sample (Sample 4).

```markdown
![Convergence Graph](https://github.com/dhaniishta/SVM-Parameter-Optimization/blob/main/graph.jpeg?raw=true)
