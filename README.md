# 🧠 Task 4: Data Imputation, Encoding & Feature Scaling – Internship Project

This notebook is the fourth task of my Artificial Intelligence internship at iGAP Technologies. The objective of this task was to preprocess a dataset by handling missing values, converting categorical features into numerical form, scaling features, and splitting the data for model training. These are foundational steps in preparing data for machine learning.

---

## 📚 Libraries Used

- **pandas** – for data manipulation  
- **numpy** – for numerical operations  
- **scikit-learn** – for preprocessing (SimpleImputer, OneHotEncoder, LabelEncoder, OrdinalEncoder, StandardScaler, train_test_split)

---

## 🧼 Key Steps Performed

### 🔧 Data Preparation

- Imported required libraries  
- Loaded the dataset using `read_csv()`  

### 📈 Handling Missing Values

- Applied `SimpleImputer(strategy='mean')` to fill missing values in numerical columns (`Age`, `Salary`)  
- Used `fit_transform()` to compute and replace missing values  

### 🔤 Categorical Encoding

#### 🏷️ One-Hot Encoding

- Applied `OneHotEncoder(sparse_output=False)` to the `Country` column  
- Used `get_feature_names_out()` to extract meaningful column names  
- Joined encoded columns back to the original dataset  
- Dropped the original `Country` column

#### 🔘 Label Encoding

- Used `LabelEncoder` on the `Purchased` column to convert Yes/No values into numeric form  
- Applied `fit_transform()` and displayed the result

#### 📶 Ordinal Encoding

- Demonstrated ordinal encoding using sample data with an inherent order  
- Used `OrdinalEncoder()` to fit and transform ordered categories  
- Printed the transformed output

---

## ⚖️ Feature Scaling

- Applied `StandardScaler` to standardize features by removing the mean and scaling to unit variance  
- Used the formula `z = (x - μ) / σ`  
- Performed:
  - `fit()` – to compute the mean and standard deviation  
  - `transform()` – to apply scaling  
  - `inverse_transform()` – to revert scaled values  
- Displayed scaled output and statistics

---

## 📂 Train-Test Split

- Divided the dataset into:
  - **Independent variables** (features)
  - **Dependent variable** (target/output)
- Used `train_test_split()` to split the data into training and testing sets  
- Printed the resulting splits to verify successful separation

---

## ✅ Final Output

- Successfully filled missing values and encoded categorical columns  
- Standardized numerical features for ML compatibility  
- Split dataset into training and testing sets, ready for model development

---

## 📂 Files

├── Task-4/
│ ├── task-4.ipynb # Notebook with full preprocessing steps
│ └── README.md # Documentation for Task 4

---

## 🏁 Status

✔️ Task 4 completed with full preprocessing  
🧪 Dataset is now ready for machine learning model training
