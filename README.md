# 🧠 Predicting Alzheimer's Disease Progression from MRI Scans and Cognitive Data

### Project Overview
This project explores a **hybrid machine learning approach** for predicting and visualizing the progression of Alzheimer’s Disease (AD) using both **numerical biomarkers** and **MRI brain scans**.  
The goal is to integrate structured cognitive data (e.g., MMSE, CDR, nWBV) with deep imaging features (CNN embeddings and texture descriptors) to derive a **Progression Index (PI)** that reflects the structural and cognitive deterioration associated with AD.

---

### 🧩 Methodology Summary

1. **Numerical Data Analysis (Random Forest)**
   - Dataset: Longitudinal ADNI-inspired tabular data.
   - Features: MMSE, CDR, nWBV, eTIV, ASF, etc.
   - Model: Random Forest Classifier for stage prediction (Normal, MCI, Demented).
   - Output: Feature importance, confusion matrix, accuracy metrics.

2. **Imaging Data Analysis (CNN + GLCM)**
   - Dataset: MRI scans (glioma, meningioma, pituitary, healthy) from Kaggle.
   - Model: Custom CNN with ReLU and max pooling layers.
   - Texture Descriptors: GLCM features (contrast, homogeneity, energy, correlation).
   - Output: Feature maps, accuracy/loss curves, and class-level activations.

3. **Hybrid Feature Fusion**
   - Combines CNN embeddings and GLCM features into a single multimodal feature space.
   - Standardized and processed for unsupervised learning.

4. **Unsupervised Progression Modeling**
   - K-Means clustering identifies three natural disease-like groups.
   - The **Progression Index (PI)** is computed as the normalized distance from the healthy cluster center.
   - PI values are categorized into:
     - **Normal (0–0.33)**
     - **MCI (0.34–0.66)**
     - **Demented (0.67–1.0)**

---

### 📊 Key Results
- **Random Forest Accuracy:** ~91%  
- **CNN Accuracy:** ~95%  
- **Progression Index Correlation:** Reflects a clear gradient of neurostructural degeneration across predicted stages.
- **Most Influential Factors:** MMSE, nWBV, and CDR for tabular model; homogeneity and contrast for imaging features.

---

### 🧠 Novel Contributions
- Developed a **hybrid multimodal fusion pipeline** integrating MRI imaging and cognitive biomarkers.
- Introduced an **unsupervised Progression Index (PI)** for label-free stage estimation.
- Combined **deep CNN embeddings** and **GLCM texture metrics** for interpretable neurodegenerative analysis.
- Proposed a practical, interpretable method to simulate Alzheimer’s progression even without paired labels.

---

