# Bank Customer Churn Prediction using Machine Learning

## 🎯 Project Goal
The goal of this project is to build a machine learning model that can accurately predict whether a bank customer will close their account (churn). By identifying customers who are at a high risk of leaving, the bank can proactively implement targeted retention strategies to improve customer loyalty and reduce financial loss.

---
## Dataset
The dataset is a CSV file (`churn.csv`) containing 10,000 records of bank customer data. Each row represents a unique customer with the following attributes:
* **Demographic Info:** `CustomerId`, `Surname`, `Geography`, `Gender`, `Age`
* **Banking Info:** `CreditScore`, `Tenure`, `Balance`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`
* **Salary Info:** `EstimatedSalary`
* **Target Variable:** `Exited` (1 if the customer churned, 0 otherwise)

---
## 🛠️ Methodology
The project followed a structured data science workflow:

1.  **Data Cleaning:** Identifier columns (`RowNumber`, `CustomerId`, `Surname`) that do not contribute predictive power were removed. The dataset was checked for missing values and found to be complete.

2.  **Exploratory Data Analysis (EDA):** Visualizations were created to uncover patterns and relationships between customer attributes and churn. Key insights were found in how churn relates to `Geography`, `Gender`, and `Age`.

3.  **Feature Engineering:** Categorical features (`Gender`, `Geography`) were converted into a numerical format using label encoding and one-hot encoding, making them suitable for machine learning models.

4.  **Model Building:** The data was split into training (80%) and testing (20%) sets. Three different classification models were built and trained using `scikit-learn` pipelines to ensure robust preprocessing (`StandardScaler`):
    * **Logistic Regression**
    * **Random Forest Classifier**
    * **Gradient Boosting Classifier**

5.  **Model Evaluation:** The models were evaluated on the unseen test data using key metrics (Accuracy, Precision, Recall, F1-Score) and confusion matrices to determine the best-performing model.

---
## 📈 Results
The Gradient Boosting model demonstrated the best performance in predicting customer churn, showing a strong balance between accuracy and the ability to correctly identify churners.

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| Logistic Regression | 0.81 | 0.59 | 0.23 | 0.33 |
| Random Forest | 0.86 | 0.76 | 0.46 | 0.57 |
| **Gradient Boosting** | **0.86** | **0.74** | **0.49** | **0.59** |

A **Feature Importance** analysis was also conducted, which revealed that `Age`, `NumOfProducts`, and `Balance` were the most influential factors in predicting churn.

---
## 💼 Business Impact
This project demonstrates the practical application of machine learning to solve a critical business problem. The predictive model built here serves as a powerful tool for the bank to **proactively identify customers at a high risk of leaving**.

By integrating this model into their operations, the bank can move from a reactive to a proactive customer retention strategy. Instead of waiting for customers to close their accounts, the bank can use the model's predictions to:
1.  **Target at-risk customers** with personalized offers, loyalty programs, or dedicated customer support.
2.  **Optimize marketing spend** by focusing retention efforts on the customers who are most likely to churn.
3.  **Gather feedback** from identified customers to better understand the root causes of churn and improve their services.

Ultimately, this data-driven approach can lead to a significant reduction in customer churn, which directly translates to increased revenue and improved long-term customer loyalty.

---
## 🚀 How to Run
1.  Clone this repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/Bank-Churn-Prediction.git](https://github.com/YOUR_USERNAME/Bank-Churn-Prediction.git)
    ```
2.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open and run the Jupyter Notebook:
    ```bash
    jupyter notebook Bank_Customer_Churn_Prediction.ipynb
    ```
