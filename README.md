# AI-Powered Predictive Maintenance: Thermography & Electrical Analysis

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat&logo=python)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange?style=flat&logo=xgboost)
![Status](https://img.shields.io/badge/Status-Industrial%20Prototype-green)

## 🚀 Executive Summary
This project implements an **end-to-end Machine Learning solution** for Industrial Predictive Maintenance (PdM). It automates the diagnosis of electrical component failures by fusing **thermographic imaging data** with **electrical magnitudes**.

Unlike traditional inspections dependent on subjective human interpretation, this model leverages **High-Dimensional Data Analysis (~76k features)** to identify fault patterns (loose contacts, overloads) with higher precision, aiming to **reduce unplanned downtime** and optimize maintenance schedules (RCM).

---

## 🏭 Industrial Challenge
**The Problem:** Thermographic interpretation is subjective, expensive, and prone to false negatives.
**The Solution:** A data-driven approach that integrates **Computer Vision concepts** and **Electrical Telemetry** to classify equipment health status objectively.

> **Key Innovation:** The model proves that adding electrical load variables to thermal data significantly reduces diagnostic uncertainty (Log Loss) compared to using thermal images alone.

---

## ⚡ Tech Stack & Tools
* **Core:** Python, NumPy, Pandas.
* **ML Engines:** XGBoost (Production Model), Scikit-learn, TensorFlow/Keras (CNN experiments).
* **Data Processing:** High-dimensional matrix manipulation for thermograms.
* **Visualization:** Matplotlib, Seaborn.

---

## ⚙️ Model Performance & Selection
Four architectures were rigorously tested for industrial viability. **XGBoost** was selected as the production model due to its superior generalization on tabular/hybrid data.

| Model | Status | Key Finding |
| :--- | :--- | :--- |
| **XGBoost** | ✅ **Selected** | **Lowest Log Loss.** Best handling of hybrid data (Thermal + Electrical). |
| **CNN** | ⚠️ Discarded | High accuracy but prone to overfitting due to dataset size constraints. |
| **Random Forest** | ❌ Discarded | Failed to effectively integrate electrical magnitude features. |
| **SVM** | ❌ Discarded | No significant improvement with added variables. |

---

## ☁️ Future Roadmap: Cloud & Azure Integration
To scale this solution for **Industry 4.0** environments, the following migration path is designed (aligned with **DP-600** & **AI-102** standards):

1.  **Data Ingestion:** Migration to **Microsoft Fabric** for real-time telemetry ingestion.
2.  **Deployment:** Serving the XGBoost model via **Azure Machine Learning** endpoints.
3.  **Visualization:** Interactive Dashboards in **Power BI** for maintenance managers.

---

## 📊 Dataset Structure
* **Input:** Thermographic matrices + Amperage/Voltage logs.
* **Complexity:** Up to ~76,800 features per sample.
* **Privacy:** *Due to industrial confidentiality, this repo contains the processing pipeline and model logic. Synthetic data is provided for demo purposes.*

---

## 📬 Author
**Michael Mancheno**
*Industrial Maintenance Engineer | Reliability & Data Specialist*
* **Focus:** Bridging the gap between Physical Asset Management and AI.
* **Contact:** [[Tu LinkedIn Aquí]](https://www.linkedin.com/in/michael-mancheno/)
