# 📊 Customer Lifetime Value (CLTV) Prediction with RFM Segmentation and XGBoost

---

## 📈 Project Overview

In modern business, understanding customer value is critical for maximizing returns on marketing investments. This project focuses on predicting **Customer Lifetime Value (CLV)**, which helps in identifying high-value customers, enhancing marketing ROI, and enabling proactive business strategies.

This analysis uses customer transaction data to engineer predictive features, perform **RFM (Recency, Frequency, Monetary) segmentation**, and build a machine learning model to forecast future customer value. The primary goal is to move beyond historical data and proactively predict which customers will be the most valuable over a future period.

---

## 🚀 Key Features

- **Advanced Feature Engineering**:  
  Creation of predictive features from raw transaction data, with focus on:
  - **Recency**: Days since the customer's last purchase  
  - **Frequency**: Total number of transactions per customer  
  - **Monetary Value**: Total revenue contributed by each customer  
  Additional metrics like average purchase value and interaction features were engineered to improve accuracy.

- **RFM Customer Segmentation**:  
  Unsupervised machine learning (**K-Means clustering**) is used to segment customers into groups based on R, F, and M scores.  
  These are combined into an overall **RFM score** to categorize customers as **Low, Mid, or High-Value**.

- **CLTV Calculation**:  
  The model predicts **6-month CLTV** using historical transaction data (3 months). This provides actionable forecasts for revenue contribution.

- **Predictive Modeling with XGBoost**:  
  An **XGBoost classifier** is trained to predict a customer’s future LTV segment (Low / Mid / High), enabling targeted marketing and retention strategies.

---

## 🛠️ Methodology

1. **Define Prediction Horizon** → 6-month prediction window selected to balance long-term and short-term insights.  
2. **Data Preparation** → Focused on UK-based customers, cleaned and preprocessed transaction dataset.  
3. **RFM Feature Engineering** → Recency, Frequency, and Monetary values calculated from a 3-month observation window.  
4. **Clustering (K-Means)** → Elbow method used to determine optimal cluster numbers; customers grouped by RFM scores.  
5. **Target Variable (CLTV)** → 6-month customer revenue computed to serve as the prediction target.  
6. **Model Training** → Features (X) and target (y) prepared; **XGBoost** trained to predict LTV segments.  
7. **Insights & Validation** → Strong correlation observed between RFM score and actual 6-month CLV, validating the model.  

---

## 💻 Technologies and Libraries Used

- **Language**: Python  
- **Libraries**:  
  - `pandas` → Data manipulation & analysis  
  - `numpy` → Numerical computations  
  - `scikit-learn` → K-Means clustering & ML utilities  
  - `xgboost` → Gradient boosting model for CLTV prediction  
- **Visualization**:  
  - `matplotlib` & `seaborn` → Data visualization  
  - `plotly` → Interactive plots  

---

## 📊 Results & Business Value

- High-value customers can be **identified and targeted** with personalized campaigns.  
- **Retention strategies** can be prioritized for mid-value customers to prevent churn.  
- Businesses can make **data-driven marketing decisions** instead of relying only on past trends.  

---

## 📂 Project Structure

├── data/ # Dataset (raw & processed)
├── notebooks/ # Jupyter/Kaggle notebooks
├── src/ # Source code (feature engineering, modeling, utils)
├── results/ # Model outputs, plots, and reports
└── README.md # Project documentation



---

## 🚧 Future Work

- Implement **survival analysis** for churn prediction  
- Test **deep learning models** for CLV forecasting  
- Integrate with a **real-time dashboard** for marketing teams  

---

## 🤝 Contributions

Contributions, issues, and feature requests are welcome!  
Feel free to fork the repo and submit a pull request.  

