# BCG X Data Science Job Simulation | PowerCo Customer Churn Prediction

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F79A3E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/Project-Completed-brightgreen?style=for-the-badge)]()

## 📌 Objective & Business Understanding
PowerCo, a major gas and electricity utility supplying small and medium-sized enterprises (SMEs), is experiencing a concerning rate of customer churn within a highly competitive energy market. 

The primary objective of this project is to apply logic and analytical precision to test the client's hypothesis: **Are customers switching providers primarily due to high price sensitivity?** By isolating the exact patterns that dictate a customer's "next move," this project develops a machine learning solution to accurately predict churn risk and deliver actionable, data-driven retention strategies.

## 📂 Data Sources
The analysis is built upon three primary datasets provided by the client:
* **Historical Customer Data:** Contains client characteristics including industry, historical electricity usage, forecasted usage, and sign-up dates.
* **Historical Pricing Data:** Contains granular records of variable and fixed pricing applied to customers at different points in time.
* **Churn Indicator:** A binary target variable indicating whether a customer has actively left the provider.

## 🧠 Strategic Methodology
This project strictly adheres to the official 5-step BCG X Data Science framework to ensure scalable and reliable business solutions:
1. **Business Understanding & Problem Framing:** Defining price sensitivity and structuring the retention problem as a binary classification task.
2. **Exploratory Data Analysis (EDA) & Data Cleaning:** Utilizing descriptive statistics and visualizations in Python to understand data types, distributions, and baseline properties.
3. **Feature Engineering:** Strategically adding, combining, and mutating raw data to enrich the dataset. A key feature developed was calculating the exact difference between off-peak prices in December and January of the preceding year to quantify true price elasticity.
4. **Predictive Modeling:** Building and training a Random Forest classifier via Scikit-Learn to identify at-risk customers.
5. **Insights & Recommendations:** Translating algorithmic outputs into clear, high-level business value for executive steering committees.

## 📊 Key Insights & Business Impact
* **The Churn Baseline:** Analysis revealed a historical churn rate of 9.7% (1,416 out of 14,606 SME customers), representing a substantial revenue leak that requires immediate intervention.
* **Hypothesis Disproven:** Contrary to PowerCo's initial assumptions, price variables exhibited a distinctly weak relationship with customer churn. Price sensitivity is not the primary driver of attrition.
* **True Churn Drivers:** The Random Forest algorithm identified that 12-month consumption volume, net margin, meter-rent, and electricity-margin are the dominant factors influencing a customer's decision to leave.
* **Strategic Pivot:** Because price is not the core issue, PowerCo must avoid implementing blanket discounts. The recommended "next move" is to deploy targeted retention outreach focused on high-value customers identified by the model.

## ⚙️ Model Performance & Next Steps
* **Current Evaluation:** The Random Forest classifier achieved a strong overall accuracy of 90.3% and a ROC-AUC score of 0.665. 
* **Area for Refinement:** The model currently exhibits a low recall score of 5.5%, meaning it is highly precise but misses a significant portion of actual churners.
* **Next Steps for Deployment:** Before pushing this model into a live production environment, it requires further iteration to address class imbalance and tune the probability thresholds. The model must ultimately be validated against a business-focused financial metric to ensure the cost of retention outreach is outweighed by the saved customer margins.
