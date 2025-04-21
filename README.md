# 🏭 Predicting Defects in Additive Manufacturing

## 📌 Project Overview
This project builds a predictive model to identify factors contributing to defect rates in **additive manufacturing (3D printing)** processes. The model helps forecast defects, enabling data-driven decisions to enhance **product quality**, **production efficiency**, and **cost-effectiveness**.

## 🎯 Aim
To accurately predict whether a product will have defects using key production parameters, and to identify the most influential features responsible for defects in 3D printing.

## 📦 Dataset
- **Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/rabieelkharoua/predicting-manufacturing-defects-dataset) by Rabie El Kharoua
- **License:** CC BY 4.0
- **Target Variable:** `Defect Status` (0 = No Defect, 1 = Defective)

## 🧠 Key Features (Sample)
- Production Volume
- Supplier Quality
- Defect Rate
- Quality Score
- Maintenance Hours
- Worker Productivity
- Safety Incidents
- Energy Consumption
- Additive Material Cost

> Dataset was highly imbalanced (more non-defect data), hence class weighting was applied.

## 📊 Correlation Analysis

### 🔝 Most Important Features (Correlated with Defect Status):
- `Maintenance Hours`: +0.30
- `Defect Rate`: +0.25
- `Quality Score`: -0.20 (higher quality = fewer defects)
- `Production Volume`: +0.13

### 🔻 Dropped Features (Correlation < |0.1|):
- `Additive Process Time`
- `Delivery Delay`
- `Energy Consumption`
- `Product Cost`, etc.

## ⚙️ Models Used
- **Logistic Regression**
- **Support Vector Machine (SVM)**

## 🧪 Model Evaluation

### Logistic Regression
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0 (No Defect) | 0.39 | 0.79 | 0.53 | 102 |
| 1 (Defective) | 0.95 | 0.77 | 0.85 | 546 |
**Accuracy:** 77%

### SVM
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0 (No Defect) | 0.41 | 0.78 | 0.54 | 102 |
| 1 (Defective) | 0.95 | 0.79 | 0.86 | 546 |
**Accuracy:** 79%

## 🧩 Inference

- **High precision (0.95)** is crucial for detecting defective items (Class 1) to avoid failures in real-world applications (especially in aerospace/healthcare).
- **Higher recall (0.79)** for both classes helps minimize false negatives (especially for defects).
- Only **4 features** (Maintenance Hours, Defect Rate, Quality Score, Production Volume) were sufficient for accurate prediction.

## ✅ Conclusion
The project demonstrates that:
- Accurate defect prediction is possible with just 4 impactful features.
- Logistic Regression and SVM provide robust and interpretable models.
- These insights can directly contribute to **higher quality control**, **cost savings**, and **safer product development** in additive manufacturing.

## 👨‍💻 Contributors
- **Aayush Raj** (22118001)  
- **Amarjeet** (22118008)  
- **Bhavesh Dubey** (22118016)  
- **Mehul Anand** (22118047)  
- **Shreyansh Verma** (22118069)

---

