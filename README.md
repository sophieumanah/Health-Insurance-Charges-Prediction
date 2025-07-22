#  Predicting Health Insurance Charges with Regression Models


Hi, in this project, I dive into the world of health insurance and build solid regression models to predict **insurance charges** based on a person’s age, lifestyle, and health indicators.

The idea is simple: given a set of demographic and health-related attributes, how accurately can I predict the insurance charges for an individual?

The notebook walks through a complete workflow — from loading and cleaning the data to exploring, modeling, and selecting the best predictive approach. Whether you're learning, hiring, or just curious, you’ll get a full picture of practical regression modelling here.

---

## 🎯 Objective

To develop a regression model that **accurately estimates health insurance charges** using a mix of demographic and behavioural features.

---

## 🧾 Dataset Overview

Here’s what we’re working with:

| Feature            | Description                                                   |
|--------------------|---------------------------------------------------------------|
| `age`              | Age of the individual (in years)                              |
| `sex`              | Gender (Male/Female)                                          |
| `bmi`              | Body Mass Index                                               |
| `children`         | Number of dependents                                          |
| `smoker`           | Smoking status (Yes/No)                                       |
| `region`           | Residential region (NE, NW, SE, SW)                           |
| `charges`          | Insurance cost in USD — **this is our target variable**       |

**Problem Type**: Supervised Regression

---

## 🧰 Tools & Libraries Used

This project was built with:

- Python 3
- `pandas`
- `numpy` 
- `matplotlib`
- `seaborn` 
- `scikit-learn`

---

## 🔍 Workflow & Approach

### 1. Initial Data Checks
- Loaded and inspected the dataset.
- Checked for missing values — turns out, none!
- Explored distributions and looked out for outliers (especially in charges).

### 2. Exploratory Data Analysis (EDA)
- Visualized key numeric variables (`age`, `bmi`, `charges`) using histograms and boxplots.
- Used countplots to explore categorical variables (`region`, `sex`, `smoker`).
- Created an `age_group` column to add more granularity to age-based insights.

### 3. Preprocessing
- Encoded categorical features using `LabelEncoder`.
- Identified features to feed into our model (dropping `charges` and `age_group` from the inputs).
- Feature scaling wasn’t strictly necessary here, but good to note for other regressors.

### 4. Modeling
Trained and compared four regression models:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Polynomial Regression (degree 2)**

Evaluation metrics used:

- **R² Score** (main metric)
- MAE, MSE, RMSE (in Jupyter Notebook)

---

## 🧠 Key Findings

| **Model**               | **Train R²** | **Test R²** | **Performance Summary**                                 |
|------------------------|--------------|-------------|---------------------------------------------------------|
| **Linear Regression**   | 0.653        | 0.697       | A reliable baseline; didn’t capture complexity          |
| **Decision Tree**       | 0.653        | 0.557       | Easy to interpret but underfitted on test data          |
| **Random Forest**       | 0.653        | 0.726       | Better generalization, reduced variance                 |
| **Polynomial Regression** | 0.653      | 0.775       | Best test performance, captured non-linear trends       |


📌 **Polynomial Regression was the top performer**, likely due to its ability to model complex patterns. Interestingly, its test performance beat the training score, which isn’t common but can happen when the test set aligns well with the learned non-linear relationships.

---

## 🧾 Conclusion

Each model brought something to the table, but the **Polynomial Regressor** outperformed the others. It demonstrates that real-world insurance data can benefit from non-linear modelling approaches, especially when human behaviours and health factors come into play.

This notebook can serve as a template for building predictive regression models, feature engineering, and evaluating models based on real-world interpretability.

---

## 💬 Got Feedback or Questions?

I’d love to hear your thoughts. Feel free to open an issue or fork the repo and build on it.  
