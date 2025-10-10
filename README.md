# 📊 Instacart Reorder Prediction  

This project predicts whether customers will reorder products in their next purchase using the **Instacart dataset**.  
It demonstrates end-to-end **data science skills**: data wrangling, EDA, feature engineering, machine learning, and business storytelling.  

---

## 🎯 Objectives  
- Explore customer purchasing behavior  
- Build features that capture **user habits** and **product characteristics**  
- Train ML models to predict reorders  
- Evaluate performance using **precision, recall, and F1-score**  
- Translate findings into **business insights**  

---

## 🛠️ Skills Demonstrated  
- Data wrangling with **pandas, numpy**  
- Visualization with **matplotlib, seaborn**  
- Feature engineering (customer & product level features)  
- Machine Learning with **scikit-learn, XGBoost/LightGBM**  
- Model evaluation (confusion matrix, precision/recall/F1)  
- Business communication & storytelling  

---

## 📂 Project Structure
```text
instacart-reorder-prediction/
├── phase1_fundamentals/      # EDA & feature engineering
├── phase2_ml_models/         # Classification, clustering, forecasting
├── phase3_advanced/          # A/B testing, CLV, recommendations
├── scripts/                  # Reusable Python scripts
├── requirements.txt          # Minimal dependencies
├── requirements-full.txt     # Full environment snapshot
└── README.md                 # Project overview (this file)
```

---

## 📈 Key Results (Phase 1: EDA)

### 🧺 Customer Ordering Patterns
- Customers typically place **10 orders** (median), with an average of ~**16 orders** each.
- A small group of **power users** place up to **100 orders** — highly engaged repeat shoppers.

### 🛒 Basket Composition
- The average basket contains **10 products**, with most customers buying **5–14 items** per order.
- The largest basket observed had **145 products** — bulk shoppers or large households.

### 🍌 Product Insights
- Most reordered product: **Banana**, followed by **Organic Banana**.
- Indicates consistent demand for staple grocery items.

### 🔁 Reordering Behavior
- Overall **reorder ratio = 59%**, meaning more than half of purchased products are repeat buys.
- This highlights **strong customer loyalty and habitual purchasing**.

🧩 *Insight:* Most customers make fewer than 20 orders, suggesting opportunities for loyalty programs targeting mid-frequency shoppers.



---
### 🔁 Reordering Behavior

- Overall **reorder ratio = 59%**, meaning more than half of all purchased products are repeat buys.
- Customers typically reorder items within **7–10 days** of their previous purchase.
- Correlation analysis revealed only **weak linear relationships** (maximum |r| ≈ 0.36), suggesting that reordering depends on **complex, non-linear interactions** among timing, product type, and customer habits.
---

# 🏁 EDA Summary

- Customers typically reorder items within **7–10 days** of their previous purchase.
- Reorders are highest on **Sundays/Mondays** at **7 AM**.  
- Correlations between numeric variables are weak, confirming **non-linear relationships** — ideal for machine learning.  
- These behavioral insights will guide **feature engineering and model design** in the next phase.

Next step → Build a baseline model to predict which products are likely to be reordered.

