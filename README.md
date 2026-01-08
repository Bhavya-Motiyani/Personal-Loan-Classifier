# Personal-Loan-Classifier
End-to-end ML project to predict personal loan acceptance for a retail bank (Thera Bank). Includes business-driven EDA, feature engineering, imbalance handling with SMOTENC, GridSearchCV tuning, model comparison, and Flask-based deployment. Optimized for high recall to minimize missed revenue opportunities.

Personal Loan Acceptance Prediction
🧠 Project Overview
| Feature              | Description                                                  |
| -------------------- | ------------------------------------------------------------ |
| **Domain**           | Banking / Predictive Analytics                               |
| **Business Problem** | Convert liability customers into personal loan customers     |
| **Goal**             | Predict which customers are likely to accept a personal loan |
| **Algorithms Used**  | Logistic Regression, Random Forest Classifier                |
| **Dataset Size**     | 5,000 customer records                                       |
| **Target Variable**  | `Personal Loan` (1 – Accepted, 0 – Not Accepted)             |
| **Deployment**       | Localhost web application                                    |


📊 Dataset Information
| Feature                | Description                             |
| ---------------------- | --------------------------------------- |
| **Source**             | Thera Bank Personal Loan Dataset        |
| **Customer Type**      | Existing depositors                     |
| **Data Nature**        | Demographic, Financial & Behavioral     |
| **Class Distribution** | ~10% positive class (highly imbalanced) |

🧾 Feature Description
| Category                | Features                                      |
| ----------------------- | --------------------------------------------- |
| **Demographics**        | Age, Experience, Family, Education            |
| **Financial**           | Income, Mortgage                              |
| **Banking Behavior**    | CCAvg, CD Account, Online, Credit Card        |
| **Engineered Features** | Age Group, CCToIncomeRatio, Mortgage Category |

🔍 Exploratory Data Analysis (EDA)
Key Insights
| Observation                                    | Business Insight                            |
| ---------------------------------------------- | ------------------------------------------- |
| Income < $50k → No loan acceptance             | Low-income customers should not be targeted |
| CD Account holders → ~6.5× acceptance          | Highest priority campaign group             |
| High income + high mortgage                    | Higher likelihood of loan acceptance        |
| Graduates & professionals dominate loan takers | Education impacts loan decisions            |
| Only ~10% acceptance rate                      | Severe class imbalance problem              |

🎯 Business Recommendations
| Focus Area       | Action                                 |
| ---------------- | -------------------------------------- |
| Income           | Target customers with income > $50,000 |
| Age Group        | Focus on customers aged 30–60          |
| Banking Products | Prioritize CD Account holders          |
| Mortgage         | Target high-mortgage customers         |
| Education        | Prefer graduates & professionals       |

🛠 Feature Engineering
| Feature           | Purpose                    |
| ----------------- | -------------------------- |
| CCToIncomeRatio   | Captures spending behavior |
| Age Group         | 20-30,30-40,etc...         |
| Mortgage Category | None,Low,Normal,High       |

🤖 Model Development
| Model                    | Preprocessing                          | Imbalance Handling | Pipeline |
| ------------------------ | -------------------------------------- | ------------------ | -------- |
| Logistic Regression      | ColumnTransformer (scaling + encoding) | SMOTENC            | Yes      |
| Random Forest Classifier | Not required                           | SMOTENC            | Yes      |

⚖️ Model Evaluation Strategy
| Metric                | Reason                           |
| --------------------- | -------------------------------- |
| Recall (Primary)      | False negatives = missed revenue |
| Confusion Matrix      | Error analysis                   |
| ROC-AUC Curve         | Threshold-independent evaluation |
| Classification Report | Overall model performance        |

🏆 Model Comparison & Selection
| Model                    | Performance Summary          |
| ------------------------ | ---------------------------- |
| Logistic Regression      | Baseline model               |
| Random Forest Classifier | Higher recall & ROC-AUC      |
| **Final Choice**         | **Random Forest Classifier** |

🚀 Deployment
| Step                | Description                   |
| ------------------- | ----------------------------- |
| Model Saving        | Serialized using `pickle`     |
| Deployment Platform | Localhost web app             |
| Prediction Type     | Real-time customer prediction |


📁 Project Structure
| Component       | Description                           |
| --------------- | ------------------------------------- |
| EDA Notebook    | Business insights & campaign strategy |
| Model Notebook  | Pipelines, training & evaluation      |
| Pickle File     | Final trained model                   |
| Deployment Code | Prediction interface                  |

🧠 Key Learnings
| Area               | Takeaway                           |
| ------------------ | ---------------------------------- |
| Business Analytics | Translating EDA into decisions     |
| ML Pipelines       | End-to-end, leakage-free modeling  |
| Imbalance Handling | Effective use of SMOTENC           |
| Model Evaluation   | Metrics aligned with business cost |
| Deployment         | From notebook to application       |

🧰 Tech Stack
| Category        | Tools                          |
| --------------- | ------------------------------ |
| Data Processing | Pandas, NumPy                  |
| Visualization   | Matplotlib, Seaborn            |
| Modeling        | Scikit-learn, Imbalanced-learn |
| Deployment      | Flask                          |
| Model Saving    | Pickle                         |

📜 License
| License     | Description                                    |
| ----------- | ---------------------------------------------- |
| MIT License | Free for learning & reference with attribution |


👩‍💻 Author

Bhavya Motiyani
B.Tech in Computer Science and Engineering
(Data Science Specialization)
Gujarat Technological University — VGEC

📧 Email: bhavyamotiyani68@gmail.com
🔗 [LinkedIn Profile](https://www.linkedin.com/in/bhavya-motiyani-059544306)
