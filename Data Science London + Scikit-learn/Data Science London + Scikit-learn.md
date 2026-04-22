# 🧠 Kaggle Machine Learning Competition Solutions

## 📊 Overview
This repository contains machine learning solutions for Kaggle-style competitions, focusing on binary classification problems using structured numerical datasets.

The main goal is to build, compare, and optimize multiple machine learning models to achieve the best performance on unseen test data.

---

## 🏆 Competition Result
- **Public Score:** 0.88301  
- **Private Score:** 0.89043  

Best performance achieved using LightGBM Classifier with cross-validation and hyperparameter tuning.

---

## 📁 Dataset Information
- **Training samples:** 1000  
- **Test samples:** 9000  
- **Features:** 40 numerical features (f0 → f39)  
- **Target:** Binary classification (0 / 1)  

📌 Note: The dataset is fully numerical with no missing values.

---

## ⚠️ Competition Environment Note
The test dataset is provided only within the competition environment and may not always be accessible locally.

Therefore, predictions are generated inside the competition platform, and only the final submission file is exported.

---

## ⚙️ Workflow

### 1. Data Loading
- Load training and test datasets using pandas
- Assign feature names (f0 → f39)
- Merge training features with labels

---

### 2. Exploratory Data Analysis (EDA)
- Correlation heatmap
- Feature distribution analysis (histograms)
- Boxplots for class separation
- Violin plots for distribution comparison
- Scatter plots for feature relationships

---

### 3. Data Preprocessing
- Verified no missing values
- Converted labels to 1D array using `.ravel()`
- Applied StandardScaler in pipelines where needed

---

### 4. Models Used
Multiple machine learning models were trained and compared:

- Logistic Regression  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Random Forest  
- Decision Tree  
- Gradient Boosting  
- AdaBoost  
- XGBoost  
- LightGBM  
- MLP Classifier  
- Gaussian Naive Bayes  

---

### 5. Model Evaluation
Models were evaluated using:
- Train/Test split (80/20)
- Accuracy Score
- 5-Fold Cross Validation

---

## 🏆 Best Model
- **Model:** LightGBM Classifier  
- **Test Accuracy:** ~0.90  
- **Cross Validation Mean:** ~0.889  

LightGBM performed the best among all tested models.

---

## 📊 Evaluation Metrics
- Accuracy Score  
- Cross Validation Score  
- Confusion Matrix  
- ROC Curve  

---

## 📤 Submission Format
Final predictions are saved in CSV format:

| Id | Solution |
|----|----------|
| 1  | 0/1      |
| 2  | 0/1      |

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  
- LightGBM  

---

## 🚀 Future Improvements
- Hyperparameter tuning (GridSearch / Optuna)
- Feature selection techniques
- Ensemble stacking models
- Advanced feature engineering

---

## 👩‍💻 Author
Machine Learning projects focused on Kaggle competitions and real-world classification problems.