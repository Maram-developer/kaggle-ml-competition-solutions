# 🚀 Spaceship Titanic - Machine Learning Project

## 📌 Project Overview

This project aims to predict whether a passenger was transported to another dimension using machine learning models.

The workflow includes:
- Data cleaning & preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model training & evaluation
- Cross-validation for reliable performance

---

## 📊 Dataset Description

The dataset is provided by the **Kaggle Spaceship Titanic competition**.

⚠️ Note:  
The dataset files are not included in this repository because they are part of an official Kaggle competition and subject to Kaggle’s rules and licensing.  
You can access the data directly from Kaggle here:  
https://www.kaggle.com/competitions/spaceship-titanic

---

### 📁 Files Overview

#### 1. train.csv
Contains personal records for about **two-thirds (~8700 passengers)** and is used for training the model.

**Features:**
- **PassengerId**: Unique ID in format `gggg_pp`
- **HomePlanet**: Planet of origin
- **CryoSleep**: Whether passenger was in suspended animation
- **Cabin**: Cabin location (`deck/num/side`)
- **Destination**: Target planet
- **Age**: Passenger age
- **VIP**: Whether passenger paid for VIP service
- **RoomService, FoodCourt, ShoppingMall, Spa, VRDeck**: Spending amounts
- **Name**: Passenger name
- **Transported**: 🎯 Target variable (True/False)

---

#### 2. test.csv
Contains about **one-third (~4300 passengers)** used for testing.

- Same features as train set (without target column)
- Goal: predict **Transported**

---

#### 3. sample_submission.csv
Template file for submission:

- PassengerId
- Transported (True/False prediction)

---

## 🧹 Data Preprocessing

- Dropped unnecessary columns (`PassengerId`, `Name`, `Cabin`)
- Handled missing values using median & categorical filling
- Converted categorical variables using encoding
- Applied **log transformation** to reduce skewness
- Handled outliers using IQR & capping

---

## ⚙️ Feature Engineering

- Created `Cabin_Name` from Cabin column
- Applied frequency encoding
- Created new feature:
  - **No_Spend** → indicates passengers with zero total spending
- Applied transformations on numerical features

---

## 🤖 Models Used

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
- Naive Bayes  

---

## 📈 Model Performance

| Model            | Accuracy | CV Mean |
|------------------|----------|----------|
| LightGBM         | 0.795    | **0.799** |
| GradientBoosting | 0.786    | 0.795 |
| SVM              | 0.782    | 0.789 |
| RandomForest     | 0.778    | 0.788 |

✔ Best Model based on Cross Validation: **LightGBM**

---

## 🏁 Final Result

The final model was submitted to Kaggle and achieved:

🏆 Public Leaderboard Score: **0.79074**

This represents the performance of the best model (LightGBM) on unseen test data.

---

## 🔍 Key Insights

- Spending features are highly important for prediction
- Feature engineering significantly improved performance
- Cross-validation gives more reliable evaluation than a single split

---

## 🧠 Future Improvements

- Hyperparameter tuning (GridSearch / Optuna)
- Advanced feature engineering
- Ensemble methods (Stacking / Blending)

---

## 💡 Conclusion

This project demonstrates a complete machine learning pipeline from raw data to prediction, achieving approximately **0.80 CV accuracy using LightGBM**.