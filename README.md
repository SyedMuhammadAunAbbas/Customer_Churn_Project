# Customer Churn Prediction

## Introduction
Customer churn refers to the rate at which customers discontinue their subscription or engagement with a service provider. It is a critical metric for businesses, directly impacting revenue and customer retention. By analyzing customer churn patterns, businesses can develop strategies to retain existing customers and improve customer satisfaction.

This project aims to predict customer churn using Machine Learning models, helping businesses identify at-risk customers and take proactive measures.

## Dataset Overview
The dataset contains customer records with various features such as:
- **Demographic Information** (Age, Gender)
- **Subscription Details** (Subscription Type, Contract Length, Total Spend)
- **Usage Patterns** (Usage Frequency, Last Interaction)
- **Customer Support Interaction** (Support Calls, Payment Delays)

The dataset consists of:
- **Training Data:** Used to train predictive models.
- **Testing Data:** 64,374 records without churn labels, used for evaluating model performance.

## Project Workflow
1. **Exploratory Data Analysis (EDA)**
   - Conducted in `Root.ipynb`
   - Analyzed dataset trends, feature importance, and visualizations.
   - Applied K-Fold cross-validation on models like SVM, Random Forest (RF), and Gaussian Naïve Bayes (GNB).

2. **Feature Engineering**
   - Tested a feature engineering approach in `improve_acc_attempt.ipynb`, which resulted in improved accuracy.

3. **Model Selection & Hyperparameter Tuning**
   - **Random Forest (RF) Optimization:** Grid Search in a separate notebook.
   - **Neural Network Experimentation:** Tested performance in another notebook.
   - **Handling Imbalance:** Applied **SMOTE** to address class imbalance.
   - **XGBoost Experimentation:** Evaluated its performance in a dedicated notebook.
   - **Final Model Selection:** Random Forest was chosen as the best-performing model.

4. **Final Model Training & Evaluation**
   - Trained and saved the best model in `FINAL_RF_MODEL_.ipynb` using **Pickle**.
   - Detailed performance evaluation documented in `DETAILED_EVALUATION_FINALE.ipynb`.

5. **Model Deployment**
   - Deployed the trained model on **localhost using Flask**.
   - Deployment files, including **HTML and CSS**, are stored in the `CHURN-PREDICTION_DEPLOY` folder.

## Technologies Used
- **Python, Pandas, NumPy, Matplotlib, Seaborn** (EDA & Preprocessing)
- **Scikit-Learn** (ML Models & Grid Search)
- **SMOTE** (Handling Class Imbalance)
- **XGBoost** (Alternative Model Experimentation)
- **Flask** (Model Deployment)
- **Pickle** (Model Saving & Loading)
- **HTML, CSS** (Web Interface for Deployment)

## Conclusion
This project successfully identifies churn-prone customers using Machine Learning techniques, enabling businesses to take data-driven retention measures. The **Random Forest model** provided the best performance and was deployed as a Flask-based web application.


