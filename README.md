# Principal Component Analysis (PCA): From Theory to Implementation

This repository contains a deep dive into **Principal Component Analysis (PCA)**, originally developed as a thesis defense for an AI/ML club. It explores the mathematical foundations, historical significance, and a practical 3D-to-2D dimensionality reduction simulation.

## 🚀 Interactive Code
The full implementation, including data generation, covariance matrix calculation, and eigenvector projection, can be found here:
**[Google Colab Notebook](https://colab.research.google.com/drive/1yB4k5GPLDmTPVJWG_cpZqZKW0fTsPsx7)**

---

## 📌 Overview
[cite_start]PCA is a systematic way to re-express high-dimensional data in a new coordinate system[cite: 46]. [cite_start]It rotates the data's basis to align with the directions of maximum variance, effectively filtering noise and revealing the true underlying structure[cite: 55, 63].

### Why This Problem Matters
[cite_start]Historically, data dimensionality has increased faster than our ability to interpret it[cite: 18]. PCA addresses several core challenges:
* [cite_start]**Visualization:** High-dimensional data is difficult for humans to see[cite: 21].
* [cite_start]**Redundancy:** Real-world measurements often contain large amounts of overlapping information[cite: 22].
* [cite_start]**Interpretability:** Raw data is usually recorded in sensor-defined coordinates rather than the system's natural coordinates[cite: 40].

---

## 🛠 The Mathematical Process
[cite_start]The implementation follows the four-step "Building Block" approach[cite: 71, 201]:

1. [cite_start]**Standardize Data:** Mean-center the data ($X_c = X - \mu$) so the average of every variable is zero[cite: 202, 206, 210].
2. [cite_start]**Compute Covariance Matrix:** Calculate $\Sigma$ to find correlations and redundancies between features[cite: 139, 203].
3. [cite_start]**Eigen Decomposition:** Decompose the matrix into **Eigenvectors** (principal directions) and **Eigenvalues** (the amount of variance/information in that direction)[cite: 196, 203, 208].
4. [cite_start]**Select & Project:** Choose the top $k$ components and project the original data into this reduced feature space ($Y = X \cdot P^T$)[cite: 81, 82, 204].



---

## 📊 Experimental Simulation: 3D to 2D
[cite_start]To demonstrate the effectiveness of PCA, the project simulates a system where three sensors measure a phenomenon that only has two degrees of freedom[cite: 256].

* [cite_start]**Input:** Correlated data points in $\mathbb{R}^3$[cite: 272, 280].
* [cite_start]**Evidence of Redundancy:** A correlation matrix shows strong coupling between variables (e.g., strong negative correlations), proving the standard basis is inefficient[cite: 306, 307].
* [cite_start]**Result:** PCA identifies the principal axes that define a 2D plane within the 3D space[cite: 336]. [cite_start]By projecting the data, we retain **>99.9% of the information** while removing 33% of the dimensions[cite: 347, 362].



---

## ⚠️ Assumptions & Limitations
[cite_start]To use PCA effectively, one must understand its underlying assumptions[cite: 24, 25]:
* [cite_start]**Linearity:** It assumes the relationship between variables is linear[cite: 253, 366].
* [cite_start]**Variance as Signal:** It assumes directions with high variance contain the most information[cite: 254, 368].
* [cite_start]**Orthogonality:** It assumes the principal components are perpendicular to one another[cite: 254, 367].
* [cite_start]**Sensitivity:** It can be highly sensitive to outliers[cite: 365, 369].

---

## 📜 Historical Legacy
[cite_start]PCA has been the gold standard for preprocessing for over a century[cite: 374]:
* [cite_start]**1901:** Karl Pearson introduces the concept of principal axes[cite: 375, 376].
* [cite_start]**1933:** Harold Hotelling mathematically formalizes the method[cite: 381].
* [cite_start]**2000s:** Becomes a standard preprocessing step in modern Machine Learning workflows[cite: 390, 391].

---

## 👤 Credits (Dimension Zero)
Ravijot Sinha
Arham Jain
Shivendu 
* [cite_start]**Theory:** Adapted from Jonathan Shlens (Google Research)[cite: 2].
* **Presentation & Implementation:** Developed for AI/ML Club Thesis Defense.
