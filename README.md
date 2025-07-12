# 🧬 Lung Cancer Prediction using Random Forest Classifier

## 📌 Project Overview

This project uses the **Random Forest Classifier** algorithm to predict the likelihood of lung cancer based on survey data. The model is trained using patient attributes such as age, smoking habits, and gender to detect lung cancer risk.

---

## 📁 Dataset Information

- **📄 File Name**: `survey lung cancer (1).csv`  
- **🎯 Target Variable**: `LUNG_CANCER` (1 = Yes, 0 = No)  
- **📊 Features**:
  - `AGE`  
  - `GENDER`  
  - `SMOKING`, `ANXIETY`, `PEER_PRESSURE`, `ALCOHOL_CONSUMING`  
  - `COUGHING`, `FATIGUE`, `SHORTNESS OF BREATH`, etc.

---

## 🧹 Data Preprocessing

1. ✅ Loaded dataset using `pandas`  
2. ❌ Checked for missing values with `.isnull().sum()`  
3. 📦 Outlier detection done using `sns.boxplot()` on `AGE`  
4. 🔁 Encoded categorical features using `LabelEncoder`:
   - `GENDER`  
   - `LUNG_CANCER`  
5. 📤 Split features (`X`) and target (`y`)

---

## 🛠️ Model Training

- 🧠 Model Used: **RandomForestClassifier**  
- 🔧 Parameters:
  - `n_estimators=10000`  
  - `max_depth=5`  
  - `random_state=40`  
  - `n_jobs=-1` (parallel processing)  
  - `oob_score=True` (Out-of-Bag error estimation)

- ✅ Training done using `clf.fit(xtrain, ytrain)`

---

## 📈 Evaluation

- 📍 Predictions made with `clf.predict(xtest)`  
- ✔️ Accuracy Score computed using `accuracy_score(ytest, ypred)`

---

## 📌 Key Observations

- 🔠 Label encoding was essential for converting text-based categories into numeric form  
- 🌲 Random Forest helps reduce overfitting and improves generalization  
- 💡 Model used Out-of-Bag score for better validation without cross-validation

---

## 🧰 Libraries Used

- `pandas` 🐼  
- `numpy` 🔢  
- `seaborn` 📊  
- `scikit-learn` 🤖

---

## 🚀 Future Enhancements

- 📊 Evaluate feature importance using `clf.feature_importances_`  
- ⚖️ Perform feature scaling and compare with other classifiers (e.g., SVM, XGBoost)  
- 🔍 Add model explainability tools like SHAP or LIME  
- 📈 Visualize ROC curve and confusion matrix  
- 💻 Build a Streamlit app for user input and prediction

---

## 🙏 Acknowledgments

- 📂 Dataset collected from a public lung cancer survey  
- 💡 Inspired by healthcare ML applications in early disease detection

---

## 📜 License

This project is licensed under the **MIT License** ✅
