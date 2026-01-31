🏥 Healthcare Operations & Patient Analytics
This project utilizes a Python-based ETL (Extract, Transform, Load) pipeline and Machine Learning to analyze hospital efficiency, identify wait-time bottlenecks, and predict patient satisfaction.

📌 Project Overview
Hospital management often struggles with "Extreme Wait Times" that lead to poor patient experiences. This project automates the cleaning of messy healthcare records and provides an interactive dashboard to visualize departmental performance.

🛠️ Tech Stack
Language: Python 3.14 (Fedora 43 Environment)

Data Manipulation: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-Learn (Random Forest Classifier)

Deployment: Streamlit (Interactive Dashboard)

🚀 The ETL Pipeline
1. Extraction
Ingested raw healthcare datasets containing patient demographics, admission timestamps, and satisfaction scores.

2. Transformation (The "Cleaning" Phase)
Feature Engineering: Merged disparate Date and Time strings into unified Python datetime objects.

Missing Value Imputation: Handled null values in categorical data and used Median Imputation for missing satisfaction scores to maintain statistical integrity.

Outlier Detection: Implemented the Interquartile Range (IQR) method to mathematically define and isolate "Extreme Wait Time" cases.
3. Loading
Exported high-performance cleaned data and specialized departmental summary reports for executive review.

🧠 Machine Learning Insights
We trained a Random Forest Classifier to predict whether a patient would report a high satisfaction score ($\ge 4$).
Key Finding: 
Wait time was the highest-weighted feature, 
proving that operational speed is the primary driver of patient happiness.
Validation: Used a 80/20 Train-Test split and evaluated performance using a Classification Report (Precision, Recall, F1-Score).

📊 Dashboard Preview
The project includes a Streamlit web application that allows users to:

Filter analytics by specific hospital departments (e.g., Orthopedics, Cardiology).

View real-time metrics for Average Wait Times vs. Satisfaction Scores.

Interact with distribution plots to see the spread of patient ages and wait durations.

💻 How to Run

Clone the repo
Install dependencies:
pip install -r requirements.txt
Run the Dashboard:
streamlit run app.py
