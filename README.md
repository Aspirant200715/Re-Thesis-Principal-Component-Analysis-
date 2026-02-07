# Principal Component Analysis (PCA): From Theory to Implementation

This repository contains a comprehensive exploration of **Principal Component Analysis (PCA)**, originally developed as a thesis defense project for an AI/ML club. It covers the mathematical foundations, historical context, and a practical 3D-to-2D dimensionality reduction simulation.

## 🚀 Interactive Code
The full implementation—including data generation, covariance matrix calculation, and eigenvector projection—is available in the interactive notebook below:
**[View PCA Implementation on Google Colab](https://colab.research.google.com/drive/1yB4k5GPLDmTPVJWG_cpZqZKW0fTsPsx7)**

---

## 📌 Project Overview
PCA is a systematic method for re-expressing high-dimensional data in a more meaningful coordinate system. By rotating the data's basis to align with the directions of maximum variance, PCA filters out noise and reveals the true underlying structure of a system.

### Core Challenges Addressed
* **High Dimensionality:** Modern data dimensionality often increases faster than our ability to interpret it.
* **Redundancy:** Real-world measurements frequently contain large amounts of overlapping information.
* **Coordinate Alignment:** Measurements are often taken in sensor-defined coordinates rather than those aligned with the true system.
* **Visualization:** High-dimensional data is difficult to visualize without loss of critical information.

---

## 🛠 The Mathematical Process
The implementation follows a principled four-step workflow:

1. **Standardize Data:** Mean-center the data ($X_c = X - \mu$) so the variables have a zero mean.
2. **Compute Covariance Matrix:** Calculate the matrix to identify redundancies and correlations between features.
3. **Eigen Decomposition:** Decompose the matrix into **Eigenvectors** (which define the new principal directions) and **Eigenvalues** (which indicate the variance captured by each direction).
4. **Select & Project:** Choose the top $k$ components and project the original data into the new $d$-dimensional coordinate system ($Y = X \cdot P^T$).

---

## 📊 Experimental Simulation: 3D to 2D
To demonstrate PCA in action, this project simulates a system where three sensors record a phenomenon that inherently has only two degrees of freedom (a mass moving on a 2D plane).

* **The Problem:** Raw observations exist in 3D space ($\mathbb{R}^3$) but are highly correlated and redundant.
* **The Analysis:** A correlation matrix confirms the linear dependence, showing that the standard basis is an inefficient way to represent the data.
* **The Result:** PCA identifies the "Principal Axes" that define the plane of motion. By projecting the data onto the first two components, we reduce the system from 3D to 2D while retaining **>99.9%** of the original information.

---

## ⚠️ Assumptions & Limitations
While PCA is a powerful tool, its effectiveness depends on several key design choices:
* **Linearity:** It assumes the relationships between variables are linear.
* **Variance as Signal:** It assumes that directions with high variance represent the signal, while low variance represents noise.
* **Orthogonality:** It assumes that principal components are perpendicular to each other.
* **Sensitivity:**
