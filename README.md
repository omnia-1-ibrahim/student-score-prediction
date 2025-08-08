# 🧠 Student Exam Score Prediction

This project is part of the **Elevvo Internship** challenge.

🎯 **Goal**: Predict students’ exam scores based on multiple factors like hours studied, teacher quality, parental involvement, sleep hours, and more.

---

## 📊 Dataset

- **Source**: [Kaggle - Student Performance Factors Dataset](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors)
- **Shape**: 500+ rows, 12+ features
- **Target**: `Exam_Score`

---

## 🔧 Tools & Libraries

- Python 🐍
- Pandas & NumPy 📊
- Matplotlib & Seaborn 📈
- Scikit-learn ⚙️

---

## 🧹 Data Preprocessing

- Handled missing values using:
  - `median` for numerical
  - `most frequent` for categorical
- Encoded categorical features using `OneHotEncoding`
- Scaled numerical features with `StandardScaler`

---

## 📈 Models Used

### ✅ Linear Regression
- Trained with full features
- Compared on different feature subsets

### 🔁 Polynomial Regression
- Used `PolynomialFeatures` with degree = 2
- Compared with linear regression to check performance gain

---

## 🧪 Evaluation Metrics

- **Mean Squared Error (MSE)**
- **R² Score**

| Feature Set                      | Model         | MSE       | R²        |
|----------------------------------|---------------|-----------|-----------|
| All Features                     | Linear        | 3.97      | 0.719     |
| All Features                     | Polynomial    | 4.13      | 0.707     |
| Without Sleep & Extracurricular | Linear        | 3.96      | 0.719     |
| Study Hours + Prev. Scores Only | Linear        | 10.54     | 0.254     |

✅ **Linear Regression performed slightly better than Polynomial in this case.**

---

## 📊 Visualizations

- Scatter plot: Hours studied vs Exam Score
- Distribution of Exam Scores
- Boxplots for categorical vs target
- Prediction comparisons

---

## 📁 Folder Structure

```bash
📦 student-exam-score-prediction/
├──  notebook.ipynb
├── README.md
