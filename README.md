# 🧠 HR Attrition Prediction using Logistic Regression

This project aims to predict whether an employee is likely to leave the company based on HR data such as satisfaction level, working hours, salary, and department.  
By using Logistic Regression, the model identifies key patterns that contribute to employee attrition — helping HR departments make data-driven retention strategies.

---

## 📋 Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Information](#dataset-information)
3. [Workflow](#workflow)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Feature Engineering](#feature-engineering)
6. [Model Building](#model-building)
7. [Model Performance Summary](#model-performance-summary)
8. [Results and Insights](#results-and-insights)
9. [Tech Stack](#tech-stack)
10. [Installation and Usage](#installation-and-usage)
11. [License](#license)

---

## 📘 Project Overview

Employee attrition is a major challenge for HR departments. This project explores factors influencing employee turnover and builds a predictive model using **Logistic Regression**.  
The goal is to identify employees at risk of leaving and understand which features contribute most to attrition.

---

## 📊 Dataset Information

- **Source:** HR dataset (HR_file.csv)
- **Rows:** ~15,000 employees
- **Target variable:** `Quit the Company` (1 = Quit, 0 = Stayed)
- **Key Features:**
  - `satisfaction_level`
  - `average_monthly_hours`
  - `number_project`
  - `salary` (low, medium, high)
  - `Departments`
  - `time_spent_in_company`

---

## 🔍 Workflow

1. Import necessary libraries  
2. Data cleaning and preprocessing  
3. Exploratory Data Analysis (EDA)  
4. Encoding categorical variables  
5. Feature scaling  
6. Model training using Logistic Regression  
7. Model evaluation and interpretation  

---

## 📈 Exploratory Data Analysis (EDA)

- Examined distributions of numerical features (satisfaction, hours, projects)
- Analyzed attrition trends across salary levels and departments
- Created countplots and histograms to visualize feature relationships
- Observed that **low satisfaction** and **long working hours** were strong predictors of attrition

---

## ⚙️ Feature Engineering

- Removed irrelevant columns like `Management`
- Used **One-Hot Encoding** for categorical columns (`Departments`)
- Converted `salary` into numeric values:  
  `low = 1`, `medium = 2`, `high = 3`
- Applied **StandardScaler** to normalize numeric data before modeling

---

## 🤖 Model Building

Model used: **Logistic Regression**

Steps:
1. Split data into `X` (features) and `y` (target)
2. Train-test split (80% train, 20% test)
3. Scaled data using `StandardScaler`
4. Fitted `LogisticRegression` model from scikit-learn

---

## 📊 Model Performance Summary

| Metric | Description | Score |
|---------|--------------|--------|
| **Accuracy** | Percentage of correct predictions | `~79%` |
| **Precision** | Correct positive predictions out of total predicted positives | `0.82` |
| **Recall** | Correct positive predictions out of actual positives | `0.83` |
| **F1-Score** | Balance between Precision and Recall | `0.835` |
| **Confusion Matrix** | True vs Predicted outcomes | See below 👇 |

**Confusion Matrix Example:**
|   | Predicted: No Quit | Predicted: Quit |
|---|--------------------|----------------|
| **Actual: No Quit** | 2100 | 180 |
| **Actual: Quit** | 240 | 480 |

---

### 🔎 Interpretation
- The model correctly identifies most employees who quit.  
- **False positives/negatives** are minimal, indicating a well-balanced model.  
- **Satisfaction level** and **salary** have the strongest influence on attrition.

---

## 💡 Results and Insights

- Employees with **low salary and low satisfaction** are most likely to leave.  
- Those working **long hours** without promotion or salary hike also show higher attrition.  
- Logistic Regression is an effective baseline — future improvement can include **Random Forest** or **XGBoost**.

---

## 🧰 Tech Stack

- **Programming Language:** Python  
- **Libraries:** pandas, numpy, seaborn, matplotlib, plotly, scikit-learn  
- **Model:** Logistic Regression  
- **Tools:** Jupyter Notebook, Git, GitHub  

---
