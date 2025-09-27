# 🚖 Predicting Taxi Collision Severity Using Pre-Trip Data

## 📌 Overview
This project applies **machine learning techniques** to predict the severity of taxi collisions in the UK using only pre-trip data (time, location, weather, driver profile, etc.).  
By enabling early risk assessment before a journey begins, the project demonstrates how ride-hailing and taxi operators can improve **safety, fleet management, and insurance strategies**.

🏆 **Achievement:** Scored the **highest mark in the cohort**.

---

## ⚙️ Methods

### Data Preparation
- Combined five years of UK road accident and vehicle data (2019–2023).  
- Focused on accidents involving taxis and private hire vehicles.  
- Pre-processed features: weather, light conditions, driver demographics, road type, region, etc.  
- Applied **KNN imputation** for missing values, **Isolation Forest** for outlier detection, and categorical encoding.  

### Exploratory Data Analysis (EDA)
- Analysed accident severity patterns across **time of day, weekdays, months, and regions**.  
- Identified high-risk patterns: **winter months, weekend nights, and rural areas**.  
- Found that **Liverpool and Westminster** were the highest-risk districts.  

### Modelling
- Framed as a **binary classification problem**: Severe (Fatal/Serious) vs Not Severe.  
- Baseline: Dummy Classifier (highlighted strong class imbalance).  
- Models tested:  
  - Logistic Regression (best recall & interpretability)  
  - Balanced Random Forest (strong recall with class imbalance handling)  
  - CatBoost, SVM, Decision Trees (for comparison)  
- **Primary metric:** Recall for severe cases (safety-first focus).  

### Hyperparameter Tuning & Validation
- Applied **GridSearchCV** with stratified cross-validation.  
- Logistic Regression: best balance of recall (0.58), interpretability, and stability.  
- Balanced Random Forest: higher recall but showed risk of overfitting.  

### Evaluation
- Used confusion matrices to compare models.  
- Feature importance analysis highlighted **day of week, region, road type, and weather** as key predictors.  
- Error analysis revealed that:  
  - False negatives often occurred in **urban daytime settings**.  
  - False positives concentrated in **deprived driver groups**.  

---

## ✅ Outcomes
Developed a **reliable predictive model** with strong recall (≈ 0.58) for severe accidents.  
Generated actionable business insights for taxi operators, including:  

- 🚦 Safer routing by avoiding high-risk times and regions.  
- 📉 Insurance cost reduction via proactive risk assessment.  
- 🧑‍🏫 Targeted driver training focused on high-risk conditions.  
- 💰 Risk-adjusted pricing for journeys in dangerous settings.  

---

## 🛠️ Skills Demonstrated
- **Machine Learning for Business Analytics**  
- **Python** (pandas, scikit-learn, CatBoost, imbalanced-learn, matplotlib, seaborn, plotly)  
- **Data Pre-processing & Cleaning** (missing values, outliers, class imbalance)  
- **Exploratory Data Analysis & Visualisation**  
- **Model Development & Tuning**  
- **Interpretability & Business Application of ML**  

---

## 📖 References
- UK Department for Transport: [Road Safety Data (2019–2023)](https://data.gov.uk/dataset/road-safety-data)  

---

✨ This project highlights the use of **machine learning for real-world, safety-critical decision making** in ride-hailing and taxi services.  
