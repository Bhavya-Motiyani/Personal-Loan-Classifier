# Personal-Loan-Classifier
End-to-end ML project to predict personal loan acceptance for a retail bank (Thera Bank). Includes business-driven EDA, feature engineering, imbalance handling with SMOTENC, GridSearchCV tuning, model comparison, and Flask-based deployment. Optimized for high recall to minimize missed revenue opportunities.

Personal Loan Acceptance Prediction
📌 Project Overview

Thera Bank has a strong base of depositors (liability customers) but relatively fewer borrowers (asset customers).
This project aims to predict which existing customers are most likely to accept a personal loan, helping the bank improve campaign targeting, reduce costs, and maximize revenue 

Personal Loan Classifier

.

The project follows a business-first, end-to-end machine learning workflow—from exploratory data analysis to model deployment.

📊 Dataset

Size: 5,000 customers

Target Variable: Personal Loan (Accepted / Not Accepted)

Features include:

Demographics: Age, Experience, Family, Education

Financials: Income, Mortgage, Credit Card Spend

Banking Behavior: CD Account, Online Banking, Credit Card usage

🔍 Exploratory Data Analysis (EDA)

EDA was performed with a business decision-making mindset, not just visualization.

Key Insights

Only customers with income > $50,000 accepted personal loans

CD Account holders are ~6.5x more likely to take a loan

High mortgage + high income customers show higher acceptance rates

Majority of loan takers are graduates or professionals

Only ~10% of customers accepted loans → severe class imbalance

Business Actions Derived

Avoid campaigning to low-income customers (< $50k)

Prioritize CD Account holders, especially via online channels

Focus on customers aged 30–60

Target high-mortgage, high-income segments

Give higher priority to graduates and professionals

EDA notebook also documents clear campaign focus groups based on these insights.

🛠 Feature Engineering

CCToIncomeRatio – proportion of income spent on credit cards

Age Groups – binned age categories

Mortgage Categories – Low / Normal / High

These features were guided by EDA findings and business relevance.

🤖 Model Development

Two models were built and compared:

1️⃣ Logistic Regression

Preprocessing using ColumnTransformer

Scaling for numerical features

Encoding for categorical features

SMOTENC used for class imbalance handling

Entire workflow wrapped in a single pipeline

2️⃣ Random Forest Classifier

No preprocessing required (tree-based model)

SMOTENC + model pipeline

Focused on capturing non-linear patterns

⚖️ Model Evaluation

Since missing a potential borrower (False Negative) is more costly than targeting the wrong customer, Recall was prioritized during model tuning.

Evaluation metrics used:

Confusion Matrix

ROC-AUC Curve

Classification Report

Result

Random Forest Classifier outperformed Logistic Regression

Higher recall and better ROC-AUC

Chosen as the final model

🚀 Model Deployment

Best-performing model saved using pickle

Deployed on a localhost web application

Enables real-time prediction using customer inputs

📁 Project Structure

EDA Notebook – Business-driven exploratory analysis & insights

Model Notebook – Feature engineering, pipelines, training & evaluation

Saved Model – Pickled final model

Deployment Code – Localhost web app for predictions

🧠 Key Learnings

Translating EDA into business actions

Handling imbalanced datasets using SMOTENC

Building leakage-free ML pipelines

Using GridSearchCV with recall-based optimization

Comparing models beyond accuracy

Deploying an ML model end-to-end

📌 Tech Stack

Python, Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn, Imbalanced-learn, Pickle, Flask

📜 License

MIT License — free to use for learning and reference with attribution
