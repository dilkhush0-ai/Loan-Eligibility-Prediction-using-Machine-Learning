# Loan Eligibility Prediction using Machine Learning

##  Project Overview

This project predicts whether a person is eligible for a loan or not using Machine Learning. The model analyzes applicant details such as Gender, Dependents, Income, Loan Amount, Credit History, and Employment status to determine loan approval.

The main goal of this project is to demonstrate how data preprocessing, feature engineering, and machine learning models can be used to solve real-world financial problems.

---

##  Features

* Data preprocessing and cleaning
* Handling missing values using mean and mode
* Encoding categorical variables using LabelEncoder
* Machine Learning model for loan prediction
* Predict whether a loan will be Approved or Not Approved

---

## 📊 Dataset Features

The model uses the following applicant details:

* Gender
* Married
* Dependents
* Education
* Self Employed
* Applicant Income
* Coapplicant Income
* Loan Amount
* Loan Amount Term
* Credit History
* Property Area

Target Variable:

* Loan Status (Approved / Not Approved)

---

## 🛠️ Data Preprocessing

Missing values were handled using mean and mode.

```python
testdata['Gender'] = testdata['Gender'].fillna(testdata['Gender'].mode()[0])
testdata['Dependents'] = testdata['Dependents'].fillna(testdata['Dependents'].mode()[0])
testdata['Self_Employed'] = testdata['Self_Employed'].fillna(testdata['Self_Employed'].mode()[0])
testdata['Loan_Amount_Term'] = testdata['Loan_Amount_Term'].fillna(testdata['Loan_Amount_Term'].mode()[0])
testdata['Credit_History'] = testdata['Credit_History'].fillna(testdata['Credit_History'].mode()[0])
testdata['LoanAmount'] = testdata['LoanAmount'].fillna(testdata['LoanAmount'].mean())
```

Categorical variables were converted to numerical values using Label Encoding.

```python
for i in range(0,5):
    test[:,i] = labelencoder_x.fit_transform(test[:,i])
```

---

## 🤖 Machine Learning Model

The project uses Machine Learning algorithms to classify loan eligibility.

Steps followed in the project:

1. Data Cleaning
2. Handling Missing Values
3. Encoding Categorical Data
4. Model Training
5. Model Prediction

---

## 📈 Goal of the Project

The goal of this project is to help financial institutions automatically determine whether a person is eligible for a loan based on their financial and personal information.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

---

## 📷 Example Output

The model predicts whether a loan is approved or not.

Example:

```
Loan Status: Approved
```

or

```
Loan Status: Not Approved
```

---

##  How to Run the Project

### 1️ Clone the repository

```
git clone https://github.com/yourusername/loan-prediction-ml.git
```

### 2️ Install required libraries

```
pip install pandas numpy scikit-learn
```

### 3️ Run the project

```
jupyter notebbok

##  Author

Created by **Dilkhush Thakur**

If you found this project useful, feel free to ⭐ star the repository.
