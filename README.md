# 🚀 Leveraging Artificial Intelligence and Open-Source Intelligence (OSINT) for Intrusion Detection

### Master of Data Science & Master of Cyber Security — Charles Darwin University  
**Authors:** Mehruz Saif, Debraj Rakshit, Md Shahriar Azad, Syed Rubayet Hossain  
**Supervisor:** Mukhtar Hussain  
**Date:** October 2025  

---

## 📘 Project Overview

This project presents a **hybrid Intrusion Detection System (IDS)** that integrates **Machine Learning (ML)** with **Open-Source Intelligence (OSINT)** to create an adaptive, context-aware cyber defense system.  
Unlike conventional IDS solutions that rely on static rule sets or manually updated signatures, this system learns dynamically from network traffic data and real-time vulnerability intelligence feeds such as the **Common Vulnerabilities and Exposures (CVE)** database, **ThreatMiner**, and **AlienVault OTX**.

The system aims to **detect both known and unknown cyberattacks** while minimizing false positives and improving recall through OSINT integration.

---

## 🎯 Objectives

1. Develop a **Machine Learning–based Intrusion Detection System (IDS)** capable of identifying and classifying cyberattacks.  
2. Integrate **real-time OSINT** data (CVE, ThreatMiner, AlienVault OTX) into the model for enhanced situational awareness.  
3. Evaluate multiple ML models — **Logistic Regression**, **Decision Tree**, **Random Forest**, and **XGBoost** — for performance and interpretability.  
4. Improve model **recall and adaptability** using OSINT-driven features.  
5. Deploy and validate the system using benchmark datasets (**KDD Cup 99**, **CICIDS 2017**) and simulated traffic.

---

## 🧠 Key Features

- **Machine Learning Integration** — supervised models trained on benchmark intrusion datasets.  
- **OSINT Fusion** — live intelligence feeds from ThreatMiner and AlienVault OTX for contextual learning.  
- **Dynamic CVE Ingestion Module** — Python-based script that automates CVE data collection and processing.  
- **Enhanced Feature Space** — inclusion of vulnerability-related metadata (e.g., exploitability, CVSS score).  
- **Model Evaluation Metrics:**  
  - Accuracy, Precision, Recall, F1-Score  
  - ROC-AUC and PR-AUC curves  
  - Confusion Matrices and Feature Importance visualizations  

---

## 🧩 Datasets Used

| Dataset | Description | Source |
|----------|--------------|--------|
| **KDD Cup 99** | Classic intrusion detection dataset with labeled network connections. | [UCI Repository](https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) |
| **CICIDS 2017** | Realistic network traffic dataset with modern attack scenarios. | [Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/ids-2017.html) |
| **Simulated Traffic** | Custom synthetic dataset created in a controlled lab environment. | Internal |

---

## ⚙️ System Architecture

```text
+-----------------------------------------------------------+
|                   Network Traffic Logs                    |
+-----------------------------------------------------------+
                 |                   |
                 v                   v
        [Preprocessing & Feature Engineering]
                 |
                 v
        [ML Models: LR, DT, RF, XGBoost]
                 |
                 v
        [OSINT Layer Integration (CVE, OTX, ThreatMiner)]
                 |
                 v
        [Hybrid ML–OSINT Intrusion Detection System]
                 |
                 v
        [Evaluation, Visualization, and Dashboard Output]

├── data/
│   ├── kddcup99.csv
│   ├── cicids2017.csv
│   └── simulated_network.csv
├── notebooks/
│   ├── KDD99_Intrusion_Detection_Final_with_OSINT_main.ipynb
├── src/
│   ├── cve_ingestion_module.py
│   ├── feature_preprocessing.py
│   ├── model_training.py
│   ├── osint_integration.py
│   └── evaluation_metrics.py
├── results/
│   ├── confusion_matrices/
│   ├── roc_curves/
│   └── feature_importance.png
├── docs/
│   └── Thesis_Final_Report_Group22.pdf
├── README.md
└── requirements.txt
