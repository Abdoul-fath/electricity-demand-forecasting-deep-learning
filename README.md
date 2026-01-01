# Electricity Demand Forecasting using Deep Learning

## 📌 Project Information
- **School**: École Nationale des Sciences Appliquées de Tétouan (ENSA Tétouan)
- **Academic Year**: 2025 – 2026
- **Module**: Deep Learning
- **Student**: Abdoulfatah Omar Hassan
- **Supervisor**: Pr. Okar

---

## 🎯 Project Objective
This project focuses on forecasting the **British electricity demand** using
advanced **Machine Learning and Deep Learning models**.
The goal is to identify the most accurate approach for short- and medium-term
electricity demand prediction in order to support intelligent power grid
management.

---

## 📊 Dataset Description
- **Source**: National Grid ESO (United Kingdom)
- **Period**: 2009 – 2024
- **Observations**: 279,264 records
- **Time resolution**: 30-minute intervals

### Main Variables
- `settlement_date`
- `settlement_period` (1–48 per day)
- `tsd` (Target System Demand – MW)
- Temporal and calendar features
- British public holidays

---

## 🧹 Data Preparation & Feature Engineering
- Removal of incoherent settlement periods (> 48)
- Removal of invalid zero-demand days
- Datetime normalization
- Temporal feature engineering (hour, day, week, season)
- Integration of UK public holidays
- Trend and seasonality analysis

---

## 🧠 Implemented Models
The following models were implemented and evaluated:

- **XGBoost**
  - Simple version
  - Optimized version (Grid Search + Cross-Validation)
- **Linear Trees**
- **Prophet**
  - Without holidays
  - With UK holidays
- **LSTM**
- **Deep LSTM**
- **Deep GRU**

---

## 📐 Evaluation Methodology
- **Train set**: 2009 – 2019  
- **Test set**: 2019 – 2021  
- **Validation set**: 2021 – 2024  

### Metrics
- **MAPE** (Mean Absolute Percentage Error)
- **RMSE** (Root Mean Square Error)

---

## 🏆 Results Summary

| Model | MAPE (%) | RMSE (MW) |
|------|----------|-----------|
| XGBoost (Simple) | 11.29 | 3786.88 |
| XGBoost (Optimized) | 7.43 | 2794.67 |
| Linear Trees | 8.49 | 3045.82 |
| Prophet | 9.37 | 3262.45 |
| Prophet + Holidays | 9.35 | 3236.63 |
| LSTM | 7.59 | 2785.54 |
| **Deep LSTM** | **7.37** | **2648.19** |
| Deep GRU | 7.62 | 2724.78 |

✅ **Best performing model: Deep LSTM**

---

## 🌐 Web Interface (IMPORTANT)
A web interface was developed to visualize predictions and interact with the models.

🔗 **Web Interface Link**:  
[https://ai.studio/apps/drive/126DTCDD60P6gzV5rTv-j-8dtVfjaYAZp](https://ai.studio/apps/drive/126DTCDD60P6gzV5rTv-j-8dtVfjaYAZp?fullscreenApplet=true)


