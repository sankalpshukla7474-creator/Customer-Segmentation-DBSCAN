# 🛒 Customer Segmentation with DBSCAN
<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
</p>

---

## 📌 Project Overview
This project implements **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** to identify distinct consumer segments within a mall's customer base. By analyzing income and spending patterns, the model discovers high-density clusters of varying shapes while effectively isolating outliers as noise.

---

## 📊 Dataset Insights
The model is trained on the **Mall Customers Dataset**, focusing on identifying economic behavior patterns.

| Feature | Details |
| :--- | :--- |
| **Source** | `Mall_Customers.csv` |
| **Data Size** | 200 customer entries |
| **Key Variables** | Annual Income ($k$), Spending Score (1-100) |
| **Goal** | Segmenting customers for targeted marketing |

---

## ⚙️ The Methodology
The pipeline follows a specialized unsupervised learning workflow designed for density detection:

### 1. Data Preprocessing
* **Feature Selection**: Dropping identifier columns like `CustomerID` and demographic data to focus on financial metrics.
* **Feature Scaling**: Normalizing data to ensure uniform distance weighting across income and spending dimensions.

### 2. Dimensionality Reduction (PCA)
* Applied **Principal Component Analysis (PCA)** to reduce the feature space to two primary components. This step enhances clustering performance and enables high-quality 2D visualization of the dense regions.

### 3. Clustering Logic
* Implementing DBSCAN by configuring the **$\epsilon$ (Epsilon)** and **min_samples** parameters.
* The model differentiates between **Core Points** (dense regions), **Border Points** (cluster edges), and **Noise Points** (statistical outliers).

---

## 📈 Results & Observations
The clustering analysis provides a clear breakdown of consumer types:

* **High-Value Segments**: Clusters representing individuals with both high income and high spending propensity.
* **Potential Growth Segments**: High-income groups with low spending scores, representing untapped marketing potential.
* **Noise Identification**: Effectively flagged anomalous data points that do not fit standard group behaviors.

> [!TIP]
> **Technical Insight**: Unlike K-Means, DBSCAN does not require a pre-specified number of clusters ($k$), making it superior for datasets where the natural group count is unknown.

---

## 🛠️ Tech Stack
* **Language**: ![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54)
* **ML Framework**: ![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikit-learn&logoColor=white)
* **Data Ops**: ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=flat&logo=numpy&logoColor=white)
* **Graphics**: ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=flat&logo=Matplotlib&logoColor=black) ![Seaborn](https://img.shields.io/badge/Seaborn-%23447091.svg?style=flat&logo=Seaborn&logoColor=white)

---

## ▶️ How to Run the Notebook

### 1. Setup
```bash
# Clone the repository
git clone <your-repo-link>
cd <repo-name>

# Install required dependencies
pip install numpy pandas scikit-learn matplotlib seaborn
