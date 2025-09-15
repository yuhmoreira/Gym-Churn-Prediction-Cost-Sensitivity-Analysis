# 📈 Gym Churn Prediction - A Machine Learning Project for Customer Retention

This project implements a machine learning workflow to **predict customer churn** for a fictional gym. By leveraging key customer behavior and demographic data, I build, evaluate, and optimize a predictive model to help the business proactively retain at-risk members.

> 🔍 **Goal:** Predict the likelihood of a customer leaving the gym (`Churn` label) and identify the most cost-effective strategy to retain them.

---

## 📊 Dataset

The dataset used is available on [Kaggle](https://www.kaggle.com/datasets/adrianvinueza/gym-customers-features-and-churn):

- `gym_churn_us.csv`: Contains customer information, contract details, and gym usage habits.
- **Target:** `Churn` (binary classification)
- **Split:** Stratified split into `"Training"` and `"Test"` sets to preserve the original class balance.

---

## 🧠 Workflow & Analysis

We follow a standard machine learning workflow, using **Logistic Regression** as a robust and interpretable model. The analysis focuses on careful feature selection and a cost-benefit analysis to find the optimal decision threshold.

### Key Steps:

- **Exploratory Data Analysis (EDA)**: Analyzed feature correlations and importance to identify the strongest churn predictors.
- **Feature Selection**: Used a Decision Tree classifier to select a subset of the most impactful features for the final model.
- **Model Training**: Trained a Logistic Regression model on the selected features.
- **Model Evaluation**: Assessed performance using key metrics like **AUC**, **PR-AUC**, and **F1-Score**, showing high and consistent results on both train and test sets.
- **Threshold Optimization**: Performed a cost-sensitive analysis to find the optimal classification threshold that minimizes business costs associated with misclassification.

---

## 📈 Key Findings

- **High Model Performance**: The model demonstrated a great performance with an **AUC of 0.97** and a **PR-AUC of 0.94**, indicating it is highly effective at distinguishing churners.
- **Actionable Threshold**: The analysis showed that a threshold of **0.2** minimizes the total cost of errors. However, due to the minimal cost difference across a range of thresholds, the business has the flexibility to choose a strategy that best fits its resources, from an aggressive approach (low threshold) to a balanced one (high threshold).

---

## 🧰 Technologies

- Python 3.8.20
- Pandas / NumPy / Seaborn / Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 🔁 Reproducibility

To run this project:

1.  Clone the repo:
    ```bash
    git clone https://github.com/yuhmoreira/Gym-Churn-Prediction-Cost-Sensitivity-Analysis.git
    cd Gym-Churn-Prediction-Cost-Sensitivity-Analysis
    ```
2.  Install dependencies from `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```
3.  Ensure your [Kaggle API key](https://www.kaggle.com/docs/api) is set up. The notebook will automatically download the dataset.

---

📌 **Highlights**

* ✅ Robust model with **0.97+ AUC** and **0.94+ PR-AUC**.
* ✅ Feature selection based on data-driven importance analysis.
* ✅ **Cost-benefit optimization** for real-world business impact.
* ✅ Complete workflow from EDA to actionable insights.
