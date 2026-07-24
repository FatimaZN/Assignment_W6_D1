# Assignment_W6_D1

Mpg Dataset- Missing Value Report


# 🚗 MPG Missing Value Report

A data cleaning and missing value analysis project completed using the **Seaborn MPG dataset**. This project explores missing values, investigates the affected column, applies an appropriate cleaning method, and compares the dataset before and after cleaning.

---

# 📖 Project Overview

The objective of this assignment was to analyze the **MPG dataset** and create a missing-value report before cleaning the data. The project demonstrates a complete data-cleaning workflow, including dataset exploration, identifying missing values, investigating the affected feature, selecting an appropriate cleaning technique, and justifying the decision based on the characteristics of the data.

---

# 🎯 Objectives

- 🔍 Explore the MPG dataset
- 📊 Identify missing values
- 📈 Analyze the affected column
- 🧹 Clean the dataset using an appropriate method
- 📝 Justify the cleaning decision
- 📋 Compare the dataset before and after cleaning

---

# 📂 Dataset Information

- **Dataset:** Seaborn MPG Dataset
- **Rows:** 398
- **Columns:** 9

## Dataset Features

- 🚗 mpg
- ⚙️ cylinders
- 🏎️ displacement
- 💨 horsepower
- ⚖️ weight
- 🚀 acceleration
- 📅 model_year
- 🌍 origin
- 🏷️ name

---

# 🛠️ Technologies Used

- 🐍 Python
- 🐼 Pandas
- 📊 Seaborn
- 📓 Jupyter Notebook

---

# 📌 Assignment Tasks

## ✅ Task 1 — Explore the Dataset

Performed an initial inspection of the dataset by:

- Viewing the dataset shape
- Listing all column names
- Checking data types using `.info()`

---

## ✅ Task 2 — Missing Value Report

Created a report showing:

- Missing value count
- Missing value percentage
- Displayed only columns with missing values
- Sorted the report from highest missing percentage to lowest

### Result

| Column     | Missing Values | Missing % |
| ---------- | -------------: | --------: |
| horsepower |              6 |      1.5% |

---

## ✅ Task 3 — Describe What You Found

Only **horsepower** column has **6 missing values** out of the total **398 rows**. This shows a very small portion (**1.5%**) of the whole dataset has missing values. It is not that serious but it is important to know how to proceed with that data either to drop it out or fill the values.

---

## ✅ Task 4 — Make a Safe Copy

Created **clean_mpg** as a copy of the original dataset before making any modifications and confirmed that both datasets contained the same number of rows.

---

## ✅ Task 5 — Investigate Before You Fill

Before deciding how to handle the missing values, the **horsepower** column was investigated by:

- 📊 Viewing summary statistics using `.describe()`
- 🧮 Calculating the mean
- 📈 Calculating the median
- 📉 Creating a histogram to understand the distribution of the data

This investigation showed that the **horsepower** column contained several outliers and extreme values. Since the mean is affected by outliers while the median is more robust, the median was chosen as the replacement value for the missing data.

---

## ✅ Task 6 — Clean the Data

The missing values in the **horsepower** column were replaced using the **median** with the `.fillna()` method.

### Cleaning Result

- Missing values before cleaning: **6**
- Missing values after cleaning: **0**

---

## ✅ Task 7 — Justify Your Decision

### ❓1. What I did

For the mpg dataset column **'Horsepower'** I filled in the missing **6 values**. I filled the values with `.fillna()` method with the **median**. This way all the **398 rows** of the dataset are preserved.

### ❓2. Why

Even though in the beginning I saw the percentage of missing value was **1.5%** comparing it to the huge dataset of **398 values** I thought it would be best to drop it but after I presented the data on a histogram I noticed that the column **horsepower** had many outliers and extreme values than normal and **mean** is sensitive to those outliers, while **median** is more reliable for those outliers. Also, the median values will ensure the dataset does not get biased by those extreme values.

### ❓3. The downside

The downside is that the median will effect the accuracy and originality of the dataset because those **6 median values** are not the correct results of horsepower for those rows.

---

## ✅ Task 8 — Before & After Summary

| Metric               | Before | After |
| -------------------- | -----: | ----: |
| Total Missing Values |      6 |     0 |
| Rows                 |    398 |   398 |
| Columns              |      9 |     9 |

---

# 🔍 Key Findings

### 📌 Finding 1

Only the **horsepower** column had **6 missing values** out of the total **398 rows**.

### 📌 Finding 2

The missing values represented only **1.5%** of the dataset, indicating that the dataset was already very clean.

### 📌 Finding 3

The histogram showed several outliers and extreme values in the **horsepower** column. Since the **mean** is affected by outliers while the **median** is more reliable, the median was chosen to replace the missing values.

---

# 💡 Skills Demonstrated

- 🐍 Python Programming
- 🐼 Data Manipulation with Pandas
- 📊 Exploratory Data Analysis (EDA)
- 🧹 Data Cleaning
- 📈 Data Visualization
- 📋 Missing Value Analysis
- 📓 Jupyter Notebook
- 💻 Git & GitHub Documentation

---

# ▶️ How to Run

1. Clone this repository.

```bash
git clone https://github.com/FatimaZN/Assignment_W6_D1.git
```

2. Open the notebook in **Jupyter Notebook** or **VS Code**.
3. Install the required libraries.

```bash
pip install pandas seaborn matplotlib
```

4. Run all notebook cells from top to bottom.

---

# 📁 Repository Structure

```text
mpg-missing-value-report/
│
├── README.md
├── mpg_missing_value_report.ipynb
└── .gitignore
```

---

# 👨‍💻 Author

Fatima Narejo

🎓 BS in Data Analytics

🐍 Python • 🐼 Pandas • 📊 Data Analysis • 📈 Data Visualization • 🧹 Data Cleaning
