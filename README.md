# project-eda-ml
Project  Mobile App Addiction Risk Predictor
# 📱 Mobile App Addiction Risk Predictor

> A Machine Learning-powered system that predicts a user's risk level of mobile app addiction — **Low**, **Medium**, or **High** — based on behavioral and demographic data.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![ML](https://img.shields.io/badge/Machine%20Learning-Scikit--learn-orange?logo=scikit-learn)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-yellow?logo=googlecolab)
![Status](https://img.shields.io/badge/Status-Final%20Year%20Project-green)

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Problem Statement](#problem-statement)
- [Tech Stack](#tech-stack)
- [Project Architecture](#project-architecture)
- [Dataset & Features](#dataset--features)
- [ML Models Used](#ml-models-used)
- [Results](#results)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Screenshots](#screenshots)
- [Future Scope](#future-scope)

---

## 📖 About the Project

Smartphone usage has skyrocketed globally, and with it, mobile app addiction has become a growing concern — particularly among students and young adults. This project applies **supervised Machine Learning** to predict an individual's addiction risk level based on their daily app usage behavior.

The system is designed as a **Final Year Engineering Project** under the domain of **Data Science**, and can assist students, parents, psychologists, and researchers in identifying and addressing problematic smartphone use early.

---

## ❓ Problem Statement

Traditional methods of identifying mobile app addiction rely on self-reported questionnaires, which are time-consuming and prone to bias. There is no fast, automated, and scalable tool available for everyday users.

**Goal:** Build a data-driven ML model that takes user behavioral inputs and classifies addiction risk into:

| Risk Level | Meaning |
|------------|---------|
| 🟢 Low | Healthy usage patterns |
| 🟡 Medium | Moderate concern; monitoring advised |
| 🔴 High | Significant addiction indicators present |

---

## 🛠️ Tech Stack

| Category | Tools / Libraries |
|----------|------------------|
| Language | Python 3.8+ |
| Environment | Google Colab / Jupyter Notebook |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Model Persistence | Joblib / Pickle |
| Deployment (Future) | Flask / Streamlit |

---

## 🏗️ Project Architecture

```
User Input
    │
    ▼
Data Collection  ──►  Data Preprocessing  ──►  Feature Engineering
                            │                          │
                    (Handle nulls,              (Correlation analysis,
                     encode, normalize)          RFE, top features)
                                                       │
                                                       ▼
                                                  ML Model Training
                                             (RF / SVM / Decision Tree)
                                                       │
                                                       ▼
                                                  Prediction Output
                                             (Low / Medium / High Risk)
                                                       │
                                                       ▼
                                               Result Dashboard
                                         (Visualization + Recommendations)
```

---

## 📊 Dataset & Features

The model is trained on a dataset of smartphone user behavioral data. Key input features include:

| Feature | Description |
|---------|-------------|
| `age` | Age of the user |
| `daily_screen_time` | Average daily screen time (hours) |
| `session_count` | Number of app sessions per day |
| `app_categories` | Types of apps used (social, gaming, OTT, etc.) |
| `notification_count` | Daily notifications received |
| `sleep_hours` | Average nightly sleep duration |
| `social_isolation_score` | Self-reported social isolation score |
| **`risk_level`** | **Target variable** — Low / Medium / High |

> Dataset is stored as a CSV file. Preprocessing steps include null handling, label encoding, and Min-Max normalization.

---

## 🤖 ML Models Used

| Model | Test Accuracy |
|-------|--------------|
| Logistic Regression | 83.0% |
| Decision Tree | 86.0% |
| Support Vector Machine (SVM) | 88.0% |
| **Random Forest** ✅ | **92.4%** |

**Best Model: Random Forest** — selected based on highest accuracy, F1-score, and 5-fold cross-validation results.

---

## 📈 Results

| Metric | Score |
|--------|-------|
| Accuracy | **92.4%** |
| Precision | **91.8%** |
| Recall | **90.5%** |
| F1-Score | **91.1%** |
| ROC-AUC | **0.96** |

**Top Predictive Features:**
1. Daily Screen Time
2. Session Frequency
3. Sleep Duration
4. Social Isolation Score

---

## 📁 Project Structure

```
project-eda-ml/
│
├── dataset/
│   └── app_usage_data.csv          # Raw dataset
│
├── notebooks/
│   └── Mobile_Addiction_Predictor.ipynb   # Main Colab notebook
│
├── models/
│   └── best_model.pkl              # Saved trained model
│
├── outputs/
│   ├── confusion_matrix.png        # Evaluation plots
│   ├── feature_importance.png
│   └── roc_curve.png
│
├── app/                            # (Future) Flask/Streamlit app
│   └── app.py
│
└── README.md
```

---

## ▶️ How to Run

### Option 1: Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `Mobile_Addiction_Predictor.ipynb`
3. Upload the dataset to `/content/` or mount Google Drive
4. Run all cells in order (`Runtime → Run All`)

### Option 2: Local (Jupyter Notebook)

**Step 1 — Clone the repository**
```bash
git clone https://github.com/your-username/project-eda-ml.git
cd project-eda-ml
```

**Step 2 — Install dependencies**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
```

**Step 3 — Launch Jupyter Notebook**
```bash
jupyter notebook notebooks/Mobile_Addiction_Predictor.ipynb
```

**Step 4 — Run all cells sequentially**

The notebook will:
- Load and preprocess the dataset
- Train multiple ML classifiers
- Display evaluation metrics and plots
- Save the best model as `best_model.pkl`

---

## 🔮 Future Scope

- 📱 **Mobile App Deployment** — Android/iOS app using Flutter + Python REST API
- 📡 **Real-Time Monitoring** — Live screen time tracking via Android UsageStatsManager
- 🧠 **Deep Learning** — LSTM model for time-series usage pattern analysis
- 💬 **NLP Integration** — Analyze social media text for behavioral addiction signals
- 🌐 **Web Dashboard** — Interactive Streamlit/Flask interface for non-technical users
- 🌍 **Global Dataset** — Expand with multi-country samples for better generalizability

---



## 📜 License

This project is developed for academic purposes as part of a Final Year Engineering Project.

---

*If you found this project helpful, please consider giving it a ⭐ on GitHub!*
