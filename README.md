# Position Salary Prediction using Decision Tree Regression

This project demonstrates how to use a **Decision Tree Regression** model to predict salaries based on position levels. It also includes a visualization of the predictions and explains why the resulting graph appears as a step function rather than a smooth curve.

---

## 📁 Dataset

The dataset used is `Position_Salaries.csv`, which contains:

- **Position Title** (ignored in this script)
- **Level** (numerical, used as the input feature `X`)
- **Salary** (used as the target variable `y`)

Example:

| Position       | Level | Salary     |
|----------------|-------|------------|
| Business Analyst | 1   | 45000      |
| CEO            | 10    | 1000000    |

---

## 🚀 Workflow

1. **Import Libraries**  
   Uses `NumPy`, `Pandas`, `Matplotlib`, and `scikit-learn`.

2. **Load Dataset**  
   Loads the position levels (`X`) and corresponding salaries (`y`).

3. **Train the Model**  
   Fits a `DecisionTreeRegressor` on the entire dataset using the `Level` as the only feature.

4. **Predict a New Result**  
   Predicts the salary for a position level of `6.5`.

5. **Visualize Results**  
   - Uses a high-resolution grid of values to illustrate how the decision tree makes predictions.
   - Shows actual data points (red dots) and predicted steps (blue line).

---

## 📈 Why the Graph is Not Smooth

Decision Trees work by **splitting the data into regions** and predicting a **constant value** in each region. This results in a **stepwise plot** instead of a continuous, smooth curve.

Additionally, since this model only uses **one independent variable (`Level`)**, it lacks additional features that might help in learning finer, smoother trends. If multiple independent variables were available (e.g., years of experience, education level, etc.), the model might generalize patterns more fluidly and reduce such abrupt steps.

---

## 🛠️ Requirements

- Python 3.x
- numpy
- pandas
- matplotlib
- scikit-learn

Install with:

```bash
pip install numpy pandas matplotlib scikit-learn
