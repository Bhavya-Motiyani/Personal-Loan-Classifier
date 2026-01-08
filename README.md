# Personal-Loan-Classifier
End-to-end ML project to predict personal loan acceptance for a retail bank (Thera Bank). Includes business-driven EDA, feature engineering, imbalance handling with SMOTENC, GridSearchCV tuning, model comparison, and Flask-based deployment. Optimized for high recall to minimize missed revenue opportunities.

Personal Loan Acceptance Prediction
📌 Project Summary
Aspect	Description
Problem	Identify depositors most likely to accept a personal loan
Goal	Improve campaign targeting and maximize loan revenue
Approach	Business-driven EDA + end-to-end ML pipelines
Outcome	Random Forest model deployed on localhost
📊 Dataset Information
Attribute	Details
Source	Thera Bank Personal Loan Dataset
Records	5,000 customers
Target Variable	Personal Loan (Accepted / Not Accepted)
Class Distribution	~10% positive class (highly imbalanced)
🧾 Feature Overview
Category	Features
Demographics	Age, Experience, Family, Education
Financial	Income, Mortgage
Banking Behavior	CCAvg, CD Account, Online, Credit Card
Engineered Features	Age Group, CCToIncomeRatio, Mortgage Category
🔍 Exploratory Data Analysis (EDA)
Key Insights
Observation	Business Interpretation
Income < $50k → No loan acceptance	Avoid campaigning low-income customers
CD Account holders → 6.5x higher acceptance	Prioritize CD customers
High income + high mortgage → high conversion	Target premium customers
Graduates & professionals dominate loan takers	Education impacts loan decisions
Only ~10% acceptance rate	Severe class imbalance
Campaign Focus Groups
Priority Segment
Income > $50,000
Age group 30–60
CD Account holders
High mortgage customers
Graduates & professionals
🛠 Feature Engineering
Feature	Purpose
CCToIncomeRatio	Measures spending behavior
Age Group	Improves interpretability
Mortgage Category	Captures risk segmentation
🤖 Model Development
Models Implemented
Model	Preprocessing	Imbalance Handling
Logistic Regression	ColumnTransformer (scaling + encoding)	SMOTENC
Random Forest Classifier	Not required	SMOTENC
Pipeline Design

Preprocessing, imbalance handling, and model combined into single pipelines

Leakage-free modeling

Hyperparameter tuning via GridSearchCV

⚖️ Model Evaluation Strategy
Metric	Reason
Recall (Priority)	False negatives = missed revenue
Confusion Matrix	Error-type analysis
ROC-AUC Curve	Threshold-independent performance
Classification Report	Overall model health
Final Model Selection
Result
Random Forest achieved higher recall and ROC-AUC
Better suited for business objective
Selected as final model
🚀 Deployment
Step	Description
Model Saving	Serialized using pickle
Deployment	Localhost web application
Usage	Real-time loan acceptance prediction
📁 Project Components
File	Purpose
EDA Notebook	Business insights & campaign strategy
Model Notebook	Feature engineering, pipelines & evaluation
Pickle File	Final trained model
Deployment Code	Localhost prediction app
🧠 Key Learnings
Area	Takeaway
Business Analytics	EDA → actionable decisions
ML Engineering	End-to-end pipelines
Imbalance Handling	SMOTENC effectiveness
Model Evaluation	Metrics aligned with business cost
Deployment	From notebook to usable product
🧰 Tech Stack
Category	Tools
Data Processing	Pandas, NumPy
Visualization	Seaborn, Matplotlib
Modeling	Scikit-learn, Imbalanced-learn
Deployment	Flask
Model Saving	Pickle
📜 License

MIT License — Free for learning and reference with attribution.

👩‍💻 Author

Bhavya Motiyani
B.Tech in Computer Science and Engineering
(Data Science Specialization)
Gujarat Technological University — VGEC

📧 Email: bhavyamotiyani68@gmail.com
🔗 [LinkedIn Profile](https://www.linkedin.com/in/bhavya-motiyani-059544306)
