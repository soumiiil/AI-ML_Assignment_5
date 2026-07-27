# Employee Attrition Prediction using Decision Tree and Random Forest

**Author:** Soumil Manhas  

**Registration Number:** 23BAI10898

**Application Number:** IN26011730

**Batch Number:** 1A

**Email ID:** manhassoumil@gmail.com

## Objective
The goal of this project is to build and compare Decision Tree and Random Forest classification models to predict employee attrition based on demographic, compensation, and job-related attributes[cite: 2].

## Dataset Link
- [Kaggle: IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)[cite: 2]

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `kaggle`

## Methodology
1. **Data Understanding**: Identified numerical and categorical attributes, confirming `Attrition` as the binary target variable[cite: 2].
2. **Data Preprocessing**:
   - Verified zero missing values[cite: 2].
   - Dropped constant/non-informative features (`EmployeeCount`, `EmployeeNumber`, `Over18`, `StandardHours`)[cite: 2].
   - Encoded binary target `Attrition` (`Yes`: 1, `No`: 0)[cite: 2].
   - One-hot encoded categorical features (`pd.get_dummies`)[cite: 2].
   - Split dataset into 80% training and 20% testing sets using stratified sampling[cite: 2].
3. **Model Development**: Trained a Decision Tree Classifier and a Random Forest Classifier (100 estimators)[cite: 2].
4. **Model Evaluation**: Evaluated using Accuracy, Precision, Recall, F1-Score, Confusion Matrices, and Feature Importance analysis[cite: 2].

## Results

| Metric | Decision Tree | Random Forest |
| :--- | :--- | :--- |
| **Accuracy** | 76.53% | **83.33%** |
| **Precision** | 31.03% | **41.67%** |
| **Recall** | **38.30%** | 10.64% |
| **F1-Score** | **34.29%** | 16.95% |

## Model Comparison
- **Accuracy & Precision**: Random Forest outperformed Decision Tree in accuracy (83.33%) and precision (41.67%), making significantly fewer false positive errors[cite: 2].
- **Recall**: Decision Tree captured more actual attrition cases (Recall: 38.30%) than standard Random Forest (10.64%), which biased predictions toward the majority class due to dataset imbalance[cite: 2].
- **Key Factors**: Feature importance analysis indicated that `MonthlyIncome`, `Age`, and `TotalWorkingYears` are the primary drivers of attrition[cite: 2].

## Conclusion
Random Forest provides superior generalization ability over single decision trees by combining predictions across an ensemble of decorrelated decision trees[cite: 2]. While single decision trees suffer from high variance and overfitting, random forests are less interpretable ("black-box")[cite: 2]. Addressing class imbalance via class weighting or SMOTE would further improve Random Forest's recall on employee churn[cite: 2].
