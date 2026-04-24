# ✈️ Flight Booking Price Prediction

> **Can we predict the price of a flight ticket before booking?**
> A full data-science pipeline — EDA, feature engineering, multicollinearity checks, and three regression models — to answer exactly that.

---

## 📌 Project Overview

| Detail | Info |
|---|---|
| **Dataset** | Flight Booking (airline, class, stops, days_left, price …) |
| **Task** | Regression — predict ticket **price** |
| **Models Used** | Linear Regression · Decision Tree · Random Forest |
| **Best R² Score** | ~0.98 (Random Forest) |
| **Language** | Python 3 |

---

## 📁 Repository Structure

```
flight-booking-price-prediction/
│
├── Flight_Booking.ipynb   
├── Flight_Booking.csv              
└── README.md
```

---

## 🔬 Methodology

### 1. 📦 Import Libraries
Standard data-science stack: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`.

### 2. 📂 Load & Explore Data
- Load the CSV and inspect shape, dtypes, and sample rows.

### 3. 🔍 Data Quality Check
- Zero missing values confirmed.
- Zero duplicate rows confirmed.

### 4. 📊 Exploratory Data Analysis (EDA)
- **Airline vs Price** — which carrier is cheapest/most expensive?
- **Days Left vs Price** — prices spike as departure approaches.
- **Airline × Class** — business class premiums across carriers.

### 5. 🔠 Feature Engineering
- Label Encoding applied to all categorical columns (airline, city, class, etc.).

### 6. 🌡️ Correlation Heatmap
- Identify features most correlated with `price`.
- Spot multicollinearity candidates.

### 7. 📐 Multicollinearity Check (VIF)
- `flight` column showed high VIF → dropped to reduce redundancy.

### 8. ✂️ Train / Test Split
- 80 / 20 split with `random_state=42`.

### 9. 🤖 Model Training & Evaluation

| Model | R² Score | Notes |
|---|---|---|
| Linear Regression | ~0.91 | Struggles with non-linearity |
| Decision Tree | ~0.97 | Good but prone to overfitting |
| **Random Forest** | **~0.98** | 🏆 Best performer |

### 10. 🏆 Model Comparison
- Visual bar chart comparing all three R² scores.

---

## 💡 Key Insights

1. **Book early** — `days_left` is one of the strongest price predictors.
2. **Business class** costs significantly more across all airlines.
3. **Random Forest** dominates thanks to ensemble averaging.
4. Linear Regression underperforms because price relationships are non-linear.

---

## 📬 Connect

If you found this project helpful, drop a ⭐ on the repo!  
Feel free to open an issue or PR for improvements.
**GitHub:** [Your GitHub]

---

*Made with 🐍 Python & ☕ coffee*
