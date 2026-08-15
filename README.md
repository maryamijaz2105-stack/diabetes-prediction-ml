# Diabetes Prediction Using Machine Learning

A machine learning project that predicts whether a patient is diabetic or non-diabetic using the **PIMA Indians Diabetes Dataset**. The project implements and compares multiple classification algorithms and selects the best-performing model based on evaluation metrics.


**Project Type:** Binary Classification
**Dataset:** PIMA Indians Diabetes Dataset

## 📌 Project Overview

The objective of this project is to develop a machine learning system that analyzes patient health-related attributes and predicts whether a patient has diabetes or not.

The project focuses on preprocessing medical data, training multiple machine learning models, evaluating their performance, and selecting the best-performing model.

## 📊 Dataset

The project uses the **PIMA Indians Diabetes Dataset**, obtained from the Kaggle Machine Learning Repository.

### Features

* Pregnancies
* Glucose
* BloodPressure
* SkinThickness
* Insulin
* BMI
* DiabetesPedigreeFunction
* Age

### Target Variable

**Outcome**

* `0` = Non-diabetic
* `1` = Diabetic

This is a **binary classification** problem.

## ⚙️ Data Preprocessing

The following preprocessing steps were applied:

* Zero values in **Glucose, BloodPressure, SkinThickness, Insulin, and BMI** were treated as missing values.
* Missing values were replaced using the mean of their respective columns.
* No encoding was required because the dataset contains no categorical variables.
* **StandardScaler** was used for feature scaling.
* The dataset was divided into:

  * **80% Training**
  * **20% Testing**
* Class distribution was visualized because the dataset contains slightly more non-diabetic cases than diabetic cases.

## 🤖 Machine Learning Models

Five classification approaches were implemented and compared:

1. **K-Nearest Neighbors (KNN)**
2. **Logistic Regression**
3. **Decision Tree**
4. **Random Forest**
5. **Artificial Neural Network (ANN)**

The models were trained using the same training dataset for comparison.

## 📈 Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

Recall was given particular importance because of the medical nature of the prediction problem.

## 🏆 Model Comparison

| Model               | Accuracy | Precision |   Recall | F1-Score |
| ------------------- | -------: | --------: | -------: | -------: |
| KNN                 |     0.76 |      0.72 |     0.68 |     0.70 |
| Logistic Regression |     0.78 |      0.74 |     0.71 |     0.72 |
| Decision Tree       |     0.74 |      0.70 |     0.69 |     0.69 |
| **Random Forest**   | **0.82** |  **0.79** | **0.76** | **0.77** |
| ANN                 |     0.80 |      0.77 |     0.74 |     0.75 |

According to the project report, **Random Forest** achieved the best overall performance and was selected as the final model.

## 🌳 Best Performing Model: Random Forest

Random Forest was selected as the final model based on its accuracy, recall, and F1-score.

The report identifies **Glucose, BMI, and Age** as the most influential features in the prediction.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* TensorFlow / Keras
* Google Colab
* Jupyter Notebook

## 📁 Project Structure

```text
diabetes-prediction-ml/
│
├── diabetes_prediction.ipynb
├── diabetes.csv
└── README.md
```

## ▶️ How to Run

1. Clone or download this repository.
2. Make sure `diabetes.csv` is in the same directory as the notebook.
3. Open `diabetes_prediction.ipynb` using Google Colab or Jupyter Notebook.
4. Install the required Python libraries if necessary.
5. Run the notebook cells from top to bottom.

The notebook loads the dataset using:

```python
df = pd.read_csv("diabetes.csv")
```
OR 

## 🔗 Google Colab

[Open Project in Google Colab](https://colab.research.google.com/drive/1XN_qo7h7LfhW3gmhODWwpMfylopQFJ3P?usp=sharing)

## 📌 Conclusion

This project demonstrates the application of machine learning classification techniques to diabetes prediction. Multiple models were implemented and compared, with Random Forest achieving the best overall performance according to the project evaluation. The project also demonstrates the importance of data preprocessing, model evaluation, and appropriate model selection in healthcare-related machine learning applications.


