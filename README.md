# linear-regression-student-performance
Predicting student academic performance using Linear Regression, Gradient Descent, and Exploratory Data Analysis.
# 🎓 Predicting Student Performance with Linear Regression

This project explores **student academic performance prediction** using the UCI "Student Performance" dataset.  
We apply **Linear Regression** using three approaches:  
- `sklearn` Linear Regression  
- Gradient Descent  
- Normal Equation  

We also conduct **statistical hypothesis tests** (Pearson correlation, t-test, ANOVA) to analyze relationships among variables.

---

## 📂 Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/student+performance)  
- **File**: `student-mat.csv`  
- **Target Variable**: `G3` (Final grade, integer 0–20)

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - One-hot encoding of categorical variables  
   - Splitting into train/test sets  
   - Scaling numerical features  

2. **Model Training**
   - Linear Regression via:
     - Sklearn API
     - Manual Gradient Descent
     - Normal Equation

3. **Evaluation Metrics**
   - R² Score
   - RMSE

4. **Statistical Analysis**
   - Pearson correlation
   - t-test
   - ANOVA

---

## 📊 Results

**Model Performance (Test Set)**  
- Sklearn Linear Regression: **R² = 0.780**, RMSE = 2.122  
- Gradient Descent: **R² = 0.780**, RMSE = 2.122  
- Normal Equation: **R² = 0.780**, RMSE = 2.122  

**Top Features by Importance**  
- `G2` (+0.978) – Strongest positive predictor  
- `failures` (−0.416) – Strong negative predictor  
- `famrel` (+0.335)  
- `age` (−0.198)  
- `Fedu` (−0.188)  

---

## 🧮 Key Equations

Linear Regression Hypothesis:  
\[
h_\theta(x) = \theta^T x
\]

Cost Function (MSE):  
\[
J(\theta) = \frac{1}{2m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2
\]

Gradient Descent Update Rule:  
\[
\theta := \theta - \alpha \frac{\partial J(\theta)}{\partial \theta}
\]

Normal Equation:  
\[
\theta = (X^T X)^{-1} X^T y
\]

---

## 📑 Hypothesis Testing
- **Pearson Correlation**: Significant positive correlation between `G2` and `G3`.  
- **t-test**: Male vs Female grades – no strong significant difference.  
- **ANOVA**: Effect of `studytime` on grades – moderate significance.  

---

## 🚀 How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
python student_performance.py

