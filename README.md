# 🔥 System Threat Forecaster

### **Can You Forewarn a System Before It’s Compromised?**

**MLP Project T12025 · Machine Learning Competition**

---

## 📌 Overview

System Threat Forecaster is a machine learning project aimed at predicting whether a computer system will get infected by malware.

The goal is to classify systems as **infected (1)** or **not infected (0)** using telemetry data collected by antivirus software.

This notebook follows the official **MLP Project T12025** competition rules.

---

## 🎯 Problem Statement

Predict whether a machine will be infected with malware based on its hardware, OS configuration, and antivirus telemetry data.

Each entry is a system uniquely identified by `MachineID`.

The label to predict is:

target = 1 → System infected

target = 0 → System clean

---

## 📊 Evaluation Metric

The leaderboard uses standard accuracy:

```python
from sklearn.metrics import accuracy_score

# Example: accuracy_score(y_true, y_pred)
```

Predictions **must be 0/1**, NOT probabilities.

---

## 🗂 Dataset Information

### Files Included

| File | Description |
|------|-------------|
| `train.csv` | Training data with features + target |
| `test.csv` | Test data without target |
| `sample_submission.csv` | Correct submission format |

---

## 🧬 Feature Summary

The dataset contains **80+ system-level features**, including:

- **Antivirus Details:** ProductName, EngineVersion, SignatureVersion
- **Security Settings:** IsBetaUser, RealTimeProtectionState, IsSystemProtected
- **OS Information:** OSVersion, OSBuildNumber, OSSkuFriendlyName
- **Processor Details:** Processor architecture, core count, manufacturer
- **Hardware Info:** Primary disk type, RAM, display resolution
- **Security Features:** SecureBoot, TPM, VirtualDevice, FirewallEnabled
- **User Locale:** CountryID, CityID, LocaleEnglishNameID
- **Timestamps:**
  - **DateAS** → Last malware signature date
  - **DateOS** → Last OS update date

---

👨‍🎓 Author

Saini Nirmal

MLP Project -T12025

System Threat Forecaster
