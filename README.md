# 🏙️ NYC Airbnb Price Classification

This project explores and applies machine learning to predict whether a New York City Airbnb listing is priced above or below **$100 per night** using listing and host features. It follows the complete ML lifecycle from problem definition to model optimization.

---

## 📌 Objective

Create a binary classification model that predicts:
- `1` if price > $100
- `0` if price ≤ $100

---

## 🧾 Dataset

- **Source**: NYC Airbnb Listings dataset (`airbnbListingsData.csv`)
- **Size**: ~28,000 listings with 50+ features
- **Label**: `price_above_100` (derived from `price` given in the data table)

---

## 🔍 Features Selected

The following features were chosen for their completeness and interpretability:

- `host_is_superhost`
- `room_type`
- `accommodates`
- `bathrooms`
- `beds`
- `bedrooms`
- `review_scores_rating`
- `review_scores_cleanliness`

Features like `description` and `host_about` were excluded due to missingness and NLP complexity.

---

## ⚙️ Workflow Summary

### ✅ Part 1–3: Setup & EDA
- Loaded and inspected the dataset
- Visualized price distribution
- Checked class balance
- Cleaned and preprocessed relevant columns

### ✅ Part 4: Project Plan
- **Data prep**: Drop nulls, one-hot encode categoricals, scale numerics
- **Modeling plan**: Train Logistic Regression → Improve with Random Forest + GridSearch
- **Evaluation**: Accuracy, F1-score, confusion matrix

### ✅ Part 5A–C: Modeling & Optimization
#### Logistic Regression:
- **Accuracy**: ~81%
- **Precision** (class 1): 83%
- **Recall** (class 1): 82%

#### Random Forest (GridSearch tuned):
- **Best params**: `{'max_depth': 10, 'min_samples_split': 2, 'n_estimators': 100}`
- **Accuracy**: ~82%
- **Precision** (class 1): 82%
- **Recall** (class 1): 84%

---

## 📈 Visualizations
- Histogram of price distribution
- Count plot for `price_above_100` classes
- Correlation heatmap with target

---

## 🧠 Models Used
- Logistic Regression (baseline)
- Random Forest Classifier (optimized via GridSearchCV)

---

## 🧪 Tools & Libraries
- Python (Pandas, NumPy)
- Scikit-learn
- Seaborn & Matplotlib

---

## 💡 Future Improvements
- Add NLP features from `description`, `neighborhood_overview`
- Use advanced models (XGBoost, LightGBM)
- Explore geospatial data like latitude/longitude

---

## 👤 Author
Harsharandeep Dhillon
