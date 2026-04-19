# 🚢 Titanic Survival Prediction

## 📌 Project Overview
This project predicts passenger survival on the Titanic dataset using multiple machine learning models. It covers data preprocessing, feature engineering, visualization, model training, and evaluation.

---

## 📊 Dataset
The dataset is from the Kaggle Titanic Competition:

🔗 [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic)

Files used:
- `train.csv`
- `test.csv`
- `gender_submission.csv`

> Note: Dataset is not included in this repository. Please download it from Kaggle.

---

## 📖 Data Dictionary

| Variable | Definition | Key |
|----------|------------|-----|
| survival | Survival | 0 = No, 1 = Yes |
| pclass | Ticket class | 1 = 1st, 2 = 2nd, 3 = 3rd |
| sex | Sex | — |
| age | Age in years | — |
| sibsp | # of siblings / spouses aboard | — |
| parch | # of parents / children aboard | — |
| ticket | Ticket number | — |
| fare | Passenger fare | — |
| cabin | Cabin number | — |
| embarked | Port of Embarkation | C = Cherbourg, Q = Queenstown, S = Southampton |

---

## ⚙️ Data Preprocessing & Feature Engineering
- Dropped irrelevant columns: `PassengerId`, `Cabin`, `Ticket`
- Extracted passenger titles from `Name` (Mr, Mrs, Rare, etc.)
- Grouped rare titles into `Rare`
- Created new features:
  - `family`: family size
  - `family_n`: (alone, small, large)
  - `child`: Age ≤ 18
  - `Fare_wealthy`: Fare > 30
- Handled missing values:
  - `Age` → median
  - `Fare` → median
- Applied One-Hot Encoding
- Aligned train/test features

---

## 📈 Data Visualization
- Correlation heatmap
- Pairplot
- Regression plots
- Boxplots

---

## 🤖 Machine Learning Models
- Logistic Regression
- SVM
- KNN
- MLP (Neural Network)
- Random Forest
- XGBoost
- LightGBM
- Gradient Boosting
- AdaBoost
- Decision Tree
- Gaussian Naive Bayes

---

## 🏆 Results

| Model         | Accuracy | CV Mean |
|--------------|----------|--------|
| MLP          | 0.849    | 0.822  |
| LGBM         | 0.843    | 0.827  |
| KNN          | 0.832    | 0.804  |
| RandomForest | 0.832    | 0.808  |

- **Best Model:** MLPClassifier  
- **Kaggle Score:** 0.77990  

---

## 🚀 How to Run
1. Open the notebook (`.ipynb`) using:
   - Google Colab (recommended)
   - Jupyter Notebook / JupyterLab
   - VS Code (with Jupyter extension)
2. Upload dataset files (`train.csv`, `test.csv`, `gender_submission.csv`)  
3. Run all cells  
4. The model will generate `submission.csv`