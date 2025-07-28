# Task-5-Exploratory-Data-Analysis-EDA-

---

## 📊 Analysis Steps

### 1. Dataset Loading
- Loaded Titanic dataset via Pandas (`read_csv`) or Seaborn's `load_dataset('titanic')`.

### 2. Data Overview
- Used:
  - `.info()` for structure
  - `.describe()` for statistics
  - `.isnull().sum()` for missing values
- Found missing values in: `age`, `embarked`, `deck`.

### 3. Univariate Analysis
- **Categorical Variables:**
  - Gender distribution
  - Passenger class
- **Numerical Variables:**
  - Age (histogram)
  - Fare (boxplot)

### 4. Bivariate & Multivariate Analysis
- Survival rate by:
  - Gender (`sns.barplot`)
  - Class (`sns.barplot`)
- Correlation matrix via `sns.heatmap`
- Visual pairplot (`sns.pairplot`) for age, fare, and survival

### 5. Visual Observations
Each chart included a written observation such as:
- Higher survival for females and first-class passengers
- Younger age groups slightly more likely to survive
- Fare and class correlate with survival

### 6. Summary of Findings
- **Sex** and **Pclass** are strong predictors of survival.
- **Children and wealthy passengers** had better survival chances.
- **Fare** has a slight positive correlation with survival.
- Dataset needs imputation for missing `age` and `embarked` values.

---

## 📸 Visuals Included

Each of these visuals is embedded in both the notebook and PDF:
- Gender Distribution (Bar Plot)
- Class Distribution (Bar Plot)
- Age Distribution (Histogram)
- Fare Distribution (Boxplot)
- Survival Rate by Gender and Class (Bar Plots)
- Correlation Heatmap
- Pairplot of Age, Fare, and Survival

---

## 📄 Report (PDF)

The `Titanic_EDA_Report.pdf` contains:
- Introduction
- Dataset overview with `.info()` and `.describe()`
- Visuals and their interpretations
- Summary of insights and findings

---


pip install pandas matplotlib seaborn jupyter
