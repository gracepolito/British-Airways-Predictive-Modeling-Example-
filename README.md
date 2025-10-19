# ✈️ British Airways – Predictive Booking Model (Forage Simulation)

This repository contains my solution to the **British Airways Data Science Virtual Internship (Forage, October 2025)**.  
The goal was to explore customer booking data and build a predictive model to estimate the likelihood of a customer completing a booking.

---

## 📊 Project Overview

### ✅ 1. Data Exploration & Preparation
- Used a dataset of **50,000 customer bookings**
- Explored data structure, missing values, and key variables
- Created new features to improve predictive power:
  - Total add-ons selected (*baggage, meals, seat preferences*)
  - Weekend vs weekday departures
  - Lead-time categories before flight
  - Trip duration and flight time features
- Applied one-hot encoding to categorical variables and scaling to numeric data

---

### ✅ 2. Machine Learning Models

| Model | Purpose | Performance (AUC) |
|-------|----------|---------------------|
| Logistic Regression | Baseline & interpretability | **0.776** |
| Logistic w/ Threshold (0.22) | Optimized recall | **Recall ↑ 10% → 63%** |
| Random Forest | Feature importance & non-linear learning | **AUC 0.78** |

---

### ✅ 3. Results & Insights

- Default Logistic Regression missed most completed bookings (low recall 0.10)
- After applying threshold tuning (0.22), recall improved to **0.63**, with an **AUC ≈ 0.78**
- Random Forest confirmed similar predictive performance and identified key features

**Top predictors of booking completion:**
- 📆 **Purchase lead time**
- ✈️ **Flight hour & flight day**
- 🛄 **Add-on purchases (baggage, seats, meals)**
- 🕒 **Length of stay / trip duration**

**Business impact:**
- Helps BA **forecast customer commitment**, **optimize resource planning**, and **target high-intent customers**.

---

## 📌 Tools Used

  - Python (Pandas, NumPy)
  - Scikit-learn (Logistic Regression, Random Forest)
  - Matplotlib, Seaborn
  - Jupyter Notebook

## 👩‍💻 Author

Grace Polito
MSc Data Science 
British Airways Data Science Virtual Experience – 2025

