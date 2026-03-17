# 🛒 Blinkit Operations Analytics – End-to-End Python Project

## 📌 Project Overview
This project implements an end-to-end **operations analytics pipeline** for Blinkit, focusing on demand forecasting, inventory risk, discount effectiveness, delivery performance, and customer satisfaction. Using Python-based machine learning models and feature engineering, the analysis provides actionable insights to reduce stockouts, improve margins, and enhance delivery reliability.

---

## 🎯 Business Problem
Blinkit faces multiple operational challenges:
- Frequent stockouts and inventory mismatches  
- Discount-driven margin erosion  
- Inconsistent delivery performance across cities  
- Declining customer satisfaction linked to delays  

This project addresses these issues through a **unified, data-driven analytics framework**.

---

## 📊 Dataset Description
- **Records:** ~13,000 products  
- **Features:** 25+ raw attributes expanded to 34 engineered features  
- **Data Includes:**  
  - Product, category, brand  
  - Pricing, discounts, profit margins  
  - Stock levels and reorder thresholds  
  - Delivery times and cities  
  - Ratings and reviews  
  - Shelf life and expiry information  

---

## 🧹 Data Preprocessing
- Standardized column names and data types  
- Converted date fields (`date_added`, `expiry_date`)  
- Handled missing values and whitespace  
- Validated data integrity using summary statistics  

---

## ⚙️ Feature Engineering
Key operational features created:
- **Days to Expiry** – expiry risk measurement  
- **Perishable Flag** – shelf-life–based classification  
- **Stockout Flag** – stock vs reorder-level indicator  
- **Revenue & Profit Value** – profitability proxies  
- **Encoded Category & City Variables** – model-ready features  
- **Discount Buckets** – elasticity analysis  

These features enable inventory, wastage, and profitability analysis at SKU level.

---

## 📈 Demand Forecasting (Regression)
**Target:** `sold_quantity`  
**Model Used:** Random Forest Regressor  

**Performance:**
- R² ≈ 0.85  
- MAE ≈ 40 units  

**Key Drivers Identified:**
- Price  
- Discount percentage  
- Stock availability  
- Demand index  
- Product category  

**Insight:**  
The model explains most demand variability and can reliably support reorder planning and inventory optimization.

---

## 📦 Stockout Risk Prediction (Classification)
**Target:** `is_stockout`  
**Model Used:** Random Forest Classifier  

**Results:**
- Clear separation driven by stock vs reorder thresholds  

**Insight:**  
Stockout behavior is strongly deterministic, enabling confident automation of replenishment decisions.

---

## 💸 Discount Elasticity Analysis
- Demand response to discounts is **non-linear**
- Different categories respond differently to promotions
- Higher discounts do not always increase profit due to margin erosion  

**Insight:**  
Uniform discounting is inefficient. Category-specific discount strategies are recommended.

---

## 🚚 Delivery Time Prediction (Regression)
**Target:** `delivery_time_min`  
**Model Used:** Random Forest Regressor  

**Performance:**
- R² ≈ 0.16  
- MAE ≈ 5 minutes  

**Insight:**  
Basic features explain delivery time directionally, but richer operational variables (traffic, distance, staffing) are needed for SLA-grade accuracy.

---

## ⭐ Customer Rating Driver Analysis (Classification)
**Target:** `low_rating_flag` (rating ≤ 3)  
**Model Used:** Logistic Regression  

**Findings:**
- Strong class imbalance (most ratings are high)
- Delivery time and discounts alone insufficient to predict dissatisfaction  

**Insight:**  
Customer satisfaction depends on qualitative factors such as product quality, substitutions, and expectation mismatch—highlighting the need for complaint and feedback data.

---

## 🧠 Key Business Insights
- Perishables carry higher stockout risk and require tighter inventory control  
- Reorder thresholds are strong predictors of shortages  
- Smarter discounting can protect margins without hurting demand  
- Delivery delays negatively impact customer ratings  
- Integrated analytics delivers more value than siloed models  

---

## 🚀 Operational Feasibility & Scalability
- Fully Python-based and dashboard-friendly  
- Can scale across cities, stores, and SKUs  
- Supports automation of daily demand forecasting and replenishment  
- Extensible into pricing, promotions, and customer experience optimization  

---

## 🔮 Future Enhancements
- Time-series forecasting (Prophet / LSTM)  
- Geo-based delivery optimization  
- NLP on customer reviews and complaints  
- Multi-objective optimization (demand, margin, SLA)  

---

## 🛠 Tools & Technologies
- **Python**
- **Pandas, NumPy**
- **Scikit-learn**
- **Matplotlib, Seaborn**
- **Jupyter Notebook**

---

## 📄 Output Artifacts
- Processed dataset with feature explanations  
- Trained models for demand, stockout, delivery, and ratings  
- Reproducible analytics pipeline  

---

## 👤 Author
**Sanskriti Dutta**  
Team SV
