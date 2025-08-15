
# 🏨 Expedia Hotel Recommendation System

## 📌 Overview
This project develops a **hotel recommendation engine** for Expedia using **XGBoost** and **Random Forest** on Kaggle’s Expedia dataset.  
The system predicts the likelihood of a user booking a hotel with **up to 95% accuracy** (XGBoost), evaluated using **F1-score, precision, recall, and confusion matrix**.  
A **Streamlit-based frontend** enables **real-time recommendations** for users.

---

## 📖 Abstract
Expedia’s platform generates vast amounts of **user-hotel interaction data**.  
Accurately predicting bookings improves **personalization** and **revenue**, reducing the time users spend searching for hotels.

**Solution Approach**:
- **Supervised Machine Learning (Classification)** to predict booking likelihood.
- **XGBoost** for high accuracy.
- **Random Forest** as a baseline.
  
**Why It Matters**:
- Reduces user search time.
- Demonstrates the impact of **boosting algorithms** in recommendation systems.

---

## 🚨 Problem Statement
### Key Issues:
- **Class Imbalance**: Few bookings vs. many clicks (~5:95 ratio).
- **High-Dimensional Data**: 50+ features including user, hotel, and search context.
- **Metric Selection**: Precision/Recall trade-off to avoid false recommendations.

**Business Impact**:
- Misrecommendations lead to **lost conversions**.

---

## 🎯 Objectives
1. **Data Preprocessing**
   - Handle missing values (e.g., `user_location` imputation).
   - Encode categorical features (`hotel_country`, `device_type`).
   
2. **Model Development**
   - Train **Random Forest** (baseline) and **XGBoost** (optimized).
   - Hyperparameter tuning (`max_depth`, `learning_rate`).

3. **Evaluation**
   - Prioritize **F1-score** over accuracy (due to imbalance).

4. **Deployment**
   - Interactive UI using **Streamlit**.

---

## ⚙️ Methodology
1. **Data Pipeline**
   - **Input**: Expedia dataset (user searches, clicks, bookings).
   - **Cleaning**: Drop duplicates, normalize numerical features (e.g., `price_usd`).
   - **Feature Engineering**: Create `time_since_last_click` for user behavior insights.
   - **Encoding**: One-hot encoding for categorical features like `hotel_chain`.

2. **Model Training**
   - **Random Forest**: 100 trees, `max_depth=10`.
   - **XGBoost**: Early stopping, `learning_rate=0.1`.
   - **Validation**: 5-fold cross-validation.

---

## 📊 Results
- **XGBoost** achieves **95% accuracy** with robust precision and recall.
- **Streamlit** provides a **user-friendly interface** for recommendations.

---

## 🚀 Next Steps
- **Cloud Deployment**: Host model on **AWS SageMaker** for scalability.
- **Real-Time Data**: Integrate with live Expedia sessions.
- **NLP Features**: Use sentiment analysis on hotel reviews for ranking.

---

## 💻 Tech Stack
- **Programming Language**: Python
- **ML Libraries**: XGBoost, Scikit-learn
- **Data Processing**: Pandas, NumPy
- **Frontend**: Streamlit
- **Visualization**: Matplotlib, Seaborn

---


---

## 🔧 Installation & Usage
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/expedia-hotel-recommendation.git
   cd expedia-hotel-recommendation

