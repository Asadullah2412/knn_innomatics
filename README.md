
---

## 📊 Diamonds Dataset and KNN from scratch

### 📌 Overview

This project uses the **Diamonds Dataset**, a well-known regression dataset commonly used for price prediction tasks. The objective is to predict the **price of a diamond** based on its physical and quality-related attributes.

---

### 🎯 Target Variable

* **Price** (7th column)
* Represents the **price of the diamond in US dollars**
* Range: **$326 – $18,823**

---

### 🧾 Dataset Characteristics

* **Data Type:** Mixed (Numerical + Categorical)
* **Total Instances:** ~54,000
* **Total Features:** 10 (excluding the target variable)

---

### 🔍 Feature Description

| Feature   | Description                           | Range / Categories                                    |
| --------- | ------------------------------------- | ----------------------------------------------------- |
| `price`   | Price in US dollars *(Target)*        | $326 – $18,823                                        |
| `carat`   | Weight of the diamond                 | 0.2 – 5.01                                            |
| `cut`     | Quality of the cut                    | Fair, Good, Very Good, Premium, Ideal                 |
| `color`   | Diamond color quality                 | J (worst) → D (best)                                  |
| `clarity` | Diamond clarity                       | I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best) |
| `x`       | Length (mm)                           | 0 – 10.74                                             |
| `y`       | Width (mm)                            | 0 – 58.9                                              |
| `z`       | Depth (mm)                            | 0 – 31.8                                              |
| `depth`   | Total depth percentage                | 43 – 79                                               |
| `table`   | Width of top relative to widest point | 43 – 95                                               |

📐 **Depth Formula:**

```
depth = 2 * z / (x + y)
```

---

### ⚠️ Important Notes

* The dataset contains **categorical features** (`cut`, `color`, `clarity`).
* These **must be encoded** (e.g., Ordinal Encoding or One-Hot Encoding) **before training any machine learning model**.
* Ensure proper preprocessing steps such as:

  * Train-test split
  * Feature scaling (if required)
  * Handling invalid zero values in dimensions (`x`, `y`, `z`)

---

### 🚀 Use Case

This dataset is ideal for:

* Regression modeling
* Feature engineering practice
* Encoding categorical variables
* Exploratory Data Analysis (EDA)

---
Here’s an **added section** you can append to your README (or place after the overview). It’s written to clearly highlight your work and learning value 👇

---

## 🛠️ Model Implementation & Evaluation

In this project, I implemented **K-Nearest Neighbors (KNN) Regression from scratch** to gain a deeper understanding of how the algorithm works internally.

### 🔧 From-Scratch KNN

* Built the KNN algorithm **without using any machine learning library**
* Implemented:

  * Distance calculation (e.g., Euclidean distance)
  * Neighbor selection based on `k`
  * Prediction logic using the average of nearest neighbors
* Used the model to predict **diamond prices**

### 📐 Evaluation Metric

* Model performance was evaluated using **Root Mean Squared Error (RMSE)**
* RMSE was chosen to directly measure how far predictions deviate from actual prices in dollar terms

### 🔍 Comparison with Scikit-learn

* Trained and evaluated a **prebuilt KNN Regressor from `scikit-learn`**
* Compared:

  * RMSE from the **custom-built KNN**
  * RMSE from **`sklearn.neighbors.KNeighborsRegressor`**
* This comparison helped validate the correctness and performance of the from-scratch implementation

### 🎯 Key Takeaway

> Implementing KNN from scratch provided strong conceptual clarity, while comparing it with scikit-learn ensured reliability and practical benchmarking.

---
