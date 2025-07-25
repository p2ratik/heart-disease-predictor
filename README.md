# 🩺 Heart Disease Prediction using Machine Learning

This project uses machine learning to predict the likelihood of heart disease in patients based on medical and demographic attributes. It involves data preprocessing, exploratory analysis, feature engineering, and evaluation of multiple classification models.

---

## 📁 Dataset

- **Source:** `heart.csv`
- **Target Column:** `HeartDisease` (1 = disease, 0 = no disease)
- **Features:**
  - Numerical (e.g., Age, Cholesterol, MaxHR, Oldpeak)
  - Categorical (e.g., Sex, ChestPainType, RestingECG)

---

## 🧪 Workflow

### 1. **Exploratory Data Analysis (EDA):**
- Visualized distributions of features using seaborn and matplotlib.
- Analyzed correlation and interactions (e.g., age vs cholesterol density).

### 2. **Preprocessing Pipeline:**
- Handled numerical and categorical features separately.
- Applied scaling (`StandardScaler`) and skew correction (`PowerTransformer`).
- Encoded categorical features using `OneHotEncoder`.
- Created a combined pipeline with `ColumnTransformer`.

### 3. **Train/Test Split:**
- Used `StratifiedShuffleSplit` on age categories to ensure balanced age distribution.
- Split: 80% training, 20% testing.

### 4. **Outlier Removal:**
- Applied IQR method for numeric columns to remove outliers in training data.

### 5. **Model Training:**
- Trained multiple classifiers using bagging:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Bagging Classifier (with base estimators)
  
### 6. **Evaluation:**
- Evaluated using 10-fold cross-validation with `neg_root_mean_squared_error` (RMSE).
- Reported average RMSE for each model.

---

## ✅ Key Results

- RMSE was used to measure average prediction error.
- Models performed with strong predictive accuracy (<10% RMSE relative to target range).
- Final pipeline is scalable and reusable.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/p2ratik/heart-disease-predictor.git
   cd heart-disease-predictor

   
