Employee Attrition Prediction Using Machine Learning

📌 Project Overview

Employee Attrition Prediction Using Machine Learning is a classification-based machine learning project developed to predict whether an employee is likely to leave an organization.

Employee attrition can significantly affect organizations through increased recruitment costs, loss of experienced employees, reduced productivity, and workforce planning challenges. This project uses machine learning algorithms to identify patterns in employee data and predict Attrition or No Attrition.

Multiple classification algorithms were trained and evaluated to determine the most suitable model for predicting employee attrition.

---

🎯 Objectives

- Predict whether an employee is likely to leave the organization.
- Apply machine learning techniques to employee-related data.
- Compare multiple classification algorithms.
- Evaluate model performance using different classification metrics.
- Identify the best-performing model for Attrition prediction.
- Analyze the importance of precision, recall, F1-score, and ROC-AUC instead of relying only on accuracy.

---

🤖 Machine Learning Models

The following algorithms were evaluated:

1. Logistic Regression

Logistic Regression is a supervised machine learning algorithm commonly used for binary classification. It predicts the probability of an employee belonging to the Attrition or No Attrition class.

2. Decision Tree

Decision Tree uses a tree-like structure of decision rules to classify employees into Attrition and No Attrition categories.

3. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to produce a final prediction.

---

📊 Dataset

The project uses employee-related data for predicting attrition.

The evaluation dataset contains:

- Total samples: 294
- No Attrition: 247
- Attrition: 47

The dataset is therefore imbalanced, with fewer Attrition cases than No Attrition cases.

---

⚙️ Project Workflow

Employee Dataset
       ↓
Data Preprocessing
       ↓
Feature Preparation
       ↓
Train/Test Data
       ↓
Model Training
       ↓
 ┌───────────────┐
 │ Logistic      │
 │ Regression    │
 ├───────────────┤
 │ Decision Tree │
 ├───────────────┤
 │ Random Forest │
 └───────────────┘
       ↓
Model Evaluation
       ↓
Performance Comparison
       ↓
Best Model Selection

---

📈 Model Performance

The models were evaluated using Accuracy, Precision, Recall, and F1-score.

Model| Accuracy| Attrition Precision| Attrition Recall| Attrition F1-score
Logistic Regression| 75.17%| 34.88%| 63.83%| 45.11%
Decision Tree| 79.00%| 38.00%| 53.00%| 44.00%
Random Forest| 84.00%| 50.00%| 15.00%| 23.00%

ROC-AUC

Logistic Regression: 0.80317

---

🏆 Best Model

Logistic Regression

Based on the project evaluation criteria, Logistic Regression was selected as the best model.

Metric| Score
Accuracy| 0.751701
Precision| 0.348837
Recall| 0.638298
F1-score| 0.451128
ROC-AUC| 0.80317

Although Random Forest achieved a higher overall accuracy of 84%, its recall for the Attrition class was only 15%.

Logistic Regression achieved an Attrition recall of 63.83%, meaning it identified a significantly larger proportion of employees who actually belonged to the Attrition class.

Therefore, Logistic Regression provides a better balance for the project's objective of identifying potential employee attrition.

---

🔍 Classification Report

Logistic Regression

Class| Precision| Recall| F1-score| Support
No Attrition| 0.92| 0.77| 0.84| 247
Attrition| 0.35| 0.64| 0.45| 47
Accuracy| | | 0.75| 294
Macro Avg| 0.63| 0.71| 0.65| 294
Weighted Avg| 0.83| 0.75| 0.78| 294

---

🧮 Confusion Matrix

The confusion matrix used in this project is:

                    Predicted
                 No          Yes

Actual No       TN          FP

Actual Yes      FN          TP

Where:

- TN (True Negative): Actual No Attrition → Predicted No Attrition
- FP (False Positive): Actual No Attrition → Predicted Attrition
- FN (False Negative): Actual Attrition → Predicted No Attrition
- TP (True Positive): Actual Attrition → Predicted Attrition

For an employee attrition prediction system, False Negatives are particularly important, because they represent employees who may leave but were incorrectly predicted as staying.

---

📋 Detailed Model Results

Logistic Regression

Accuracy      : 0.751701
Precision     : 0.348837
Recall        : 0.638298
F1 Score      : 0.451128
ROC-AUC       : 0.803170

Decision Tree

Accuracy      : 0.790000
Precision     : 0.380000
Recall        : 0.530000
F1 Score      : 0.440000

Random Forest

Accuracy      : 0.840000
Precision     : 0.500000
Recall        : 0.150000
F1 Score      : 0.230000

---

💡 Why Accuracy Alone Is Not Enough

The dataset contains significantly more No Attrition cases than Attrition cases.

Because of this imbalance, a model can achieve high overall accuracy while performing poorly on the Attrition class.

For example, Random Forest achieved:

«84% Accuracy»

However, its Attrition recall was only:

«15%»

This means the model correctly identified only a small proportion of the actual Attrition cases.

Logistic Regression achieved lower overall accuracy but much better Attrition recall:

«63.83% Attrition Recall»

Therefore, this project considers F1-score and ROC-AUC, along with the minority-class recall, when selecting the final model.

---

🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

---

📂 Project Structure

Employee-Attrition-Prediction/
│
├── dataset/
│   └── employee_attrition.csv
│
├── notebooks/
│   └── employee_attrition_prediction.ipynb
│
├── models/
│   └── logistic_regression_model.pkl
│
├── images/
│   ├── confusion_matrix.png
│   └── model_comparison.png
│
├── README.md
└── requirements.txt

---

🚀 Installation

Clone the repository:

git clone <your-repository-url>

Navigate to the project directory:

cd Employee-Attrition-Prediction

Install the required Python libraries:

pip install -r requirements.txt

---

▶️ How to Run

Open the Jupyter Notebook:

jupyter notebook

Then open:

employee_attrition_prediction.ipynb

Run the cells sequentially to:

1. Load the dataset
2. Perform data preprocessing
3. Prepare the features
4. Train the machine learning models
5. Evaluate the models
6. Compare their performance
7. Select the best model

---

📊 Key Findings

- Random Forest achieved the highest overall accuracy (84%).
- Logistic Regression achieved the highest Attrition recall (63.83%).
- Logistic Regression achieved the highest Attrition F1-score (45.11%) among the evaluated models.
- Logistic Regression achieved a ROC-AUC of 0.80317.
- The dataset contains an imbalance between Attrition and No Attrition cases.
- Accuracy alone is not sufficient to determine the best model.
- Logistic Regression was selected as the final model based on F1-score and ROC-AUC.

---

🔮 Future Enhancements

The project can be further improved by:

- Applying class-balancing techniques such as SMOTE or class weights.
- Performing hyperparameter tuning.
- Using cross-validation for more reliable evaluation.
- Testing additional algorithms such as XGBoost and Gradient Boosting.
- Deploying the model as a web application.
- Creating an interactive employee attrition prediction dashboard.
- Adding explainable AI techniques to understand individual predictions.
- Continuously monitoring model performance using new employee data.

---

⚠️ Limitations

- The dataset contains class imbalance.
- The prediction quality depends on the available employee features.
- The model should be validated using additional real-world data before deployment.
- Machine learning predictions should be used as decision-support information rather than as the sole basis for employee-related decisions.

---

🎓 Internship Project

This project was developed as part of an internship project to demonstrate the practical application of machine learning in solving a real-world business problem.

The project covers the complete machine learning workflow, including data preparation, model development, performance evaluation, comparison, and model selection.

---

📜 Conclusion

The Employee Attrition Prediction Using Machine Learning project demonstrates how supervised machine learning can be used to predict potential employee attrition.

Three classification algorithms — Logistic Regression, Decision Tree, and Random Forest — were evaluated. While Random Forest achieved the highest overall accuracy, Logistic Regression demonstrated better performance for identifying the Attrition class based on recall and F1-score and achieved a ROC-AUC of 0.80317.

Based on the evaluation criteria, Logistic Regression was selected as the final model for the project.

This project highlights the importance of selecting evaluation metrics according to the actual problem objective rather than depending solely on overall accuracy.

---

👨‍💻 Author

Employee Attrition Prediction Using Machine Learning

Internship Project
