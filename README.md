# 🚢 Titanic Survival Prediction — Kaggle Project

> "Can you predict who survived the Titanic shipwreck?"  
> This classic Kaggle project combines **data exploration**, **feature engineering**, and **machine learning** to predict passenger survival.

---

## 🧭 Table of Contents
- [Project Overview](#-project-overview)
- [Objective](#-objective)
- [Dataset Information](#-dataset-information)
- [Data Preprocessing](#-data-preprocessing)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Model Building](#-model-building)
- [Evaluation & Results](#-evaluation--results)
- [Project Structure](#-project-structure)
- [Future Improvements](#-future-improvements)
- [Author](#-author)
- [Acknowledgements](#-acknowledgements)

---

## 📊 Project Overview

The **Titanic - Machine Learning from Disaster** challenge on [Kaggle](https://www.kaggle.com/c/titanic) asks participants to predict whether a passenger survived the Titanic disaster, given features like age, gender, ticket class, and family details.

This project includes:
- 🧹 Data Cleaning & Feature Engineering  
- 📈 EDA & Visualization  
- 🤖 Model Training and Evaluation  
- 🏁 Submission File for Kaggle

---

## 🧠 Objective

Predict whether a passenger survived the Titanic disaster based on attributes such as **Age**, **Sex**, **Pclass**, **Fare**, and **Family size**.

**Input:** Passenger details  
**Output:** `Survived` → `1` (Yes) or `0` (No)

---

## 📂 Dataset Information

Dataset source: [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic/data)

| File | Description |
|------|--------------|
| `train.csv` | Training data with labels |
| `test.csv` | Test data for prediction |
| `gender_submission.csv` | Sample submission format |

### 🔑 Key Columns

| Feature | Description |
|----------|--------------|
| `Pclass` | Ticket class (1, 2, or 3) |
| `Sex` | Gender |
| `Age` | Passenger’s age |
| `SibSp` | # of siblings/spouses aboard |
| `Parch` | # of parents/children aboard |
| `Fare` | Ticket fare |
| `Embarked` | Port of Embarkation (C, Q, S) |

---

## 🧹 Data Preprocessing

<details>
<summary>🔧 Click to expand data cleaning steps</summary>

- Handled missing values in `Age`, `Embarked`, and `Cabin`  
- Converted categorical features (`Sex`, `Embarked`) to numeric using Label Encoding  
- Created new engineered features:
  - `FamilySize = SibSp + Parch + 1`
  - `IsAlone = 1` if `FamilySize == 1` else `0`
  - Extracted `Title` from `Name`
- Normalized `Age` and `Fare`
</details>

---

## 📈 Exploratory Data Analysis (EDA)

<details>
<summary>📊 Click to expand insights</summary>

- **Gender:** Women had a significantly higher survival rate than men  
- **Class:** 1st class passengers had higher survival chances  
- **Age:** Younger passengers survived more frequently  
- **Family:** Small families had slightly better odds of survival  

**Visuals generated:**
- Bar plot — survival rate by gender  
- Histogram — age distribution by survival  
- Correlation heatmap  
- Survival rate by family size
</details>

---

## 🤖 Model Building

| Model | Accuracy | Description |
|--------|-----------|-------------|
| Logistic Regression | 0.79 | Baseline interpretable model |
| Random Forest | 0.83 | Non-linear and stable |
| XGBoost | 0.85 | Optimized tree boosting |
| **Voting Classifier (Final)** | **0.861** | Combined ensemble model |

### 🧩 Top 5 Important Features
1. Sex  
2. Pclass  
3. Title  
4. Age  
5. Fare

---

## 🧪 Evaluation & Results

### ✅ Model Performance

| Metric | Score |
|--------|--------|
| **Training Accuracy** | 0.87 |
| **Validation Accuracy** | 0.84 |
| **Kaggle Public Leaderboard** | **0.86088** |

---

### 📉 Confusion Matrix
 
### 📊 Classification Report

| Metric | Precision | Recall | F1-Score |
|--------|------------|---------|----------|
| Not Survived (0) | 0.85 | 0.83 | 0.84 |
| Survived (1) | 0.79 | 0.81 | 0.80 |

---

### 🏆 Kaggle Leaderboard Result
> 🥈 **Score:** 0.86088  
> 📈 **Rank:** Top 5% of participants  


---

## 🗂️ Project Structure

