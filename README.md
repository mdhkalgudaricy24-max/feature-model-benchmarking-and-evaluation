# feature-model-benchmarking-and-evaluation

TransferIQ: Dynamic Player Transfer Value Prediction
TransferIQ is an advanced AI-driven system developed during my internship to estimate football player market values. By integrating multi-source data including performance statistics, social media sentiment, and injury history, the project provide a data-driven approach to player valuation.
📌 Project Overview
The objective was to move beyond basic performance metrics and incorporate "Dynamic" factors—like public perception and injury risk—into a robust machine learning pipeline. The project focuses on predicting Transfermarkt Estimated Market Values with high accuracy and explainability.
📊 Multi-Source Data Integration
The dataset consists of 450+ players with features merged from:
Performance Metrics: Aggregated data (Goals, Assists, Passing Accuracy, Defensive Index).
Social Media Sentiment: NLP-processed scores from player mentions to quantify public perception.
Injury Records: Historical data used to calculate injury risk and recovery time impacts.
🛠️ Technical Implementation
Data Cleaning & Integrity: Following industry standards, all features with a correlation greater than 0.9 (e.g., pre-calculated performance scores) were removed to prevent Data Leakage and ensure the model learned from raw indicators.
Feature Engineering: Applied Log-Transformation to the target variable to normalize the valuation of "Superstar" players and created interaction features to capture the relationship between efficiency and market value.
Preprocessing: Implemented a full pipeline using StandardScaler for feature normalization and LabelEncoder for categorical variables.
🏆 Model Benchmarking & Evaluation
I conducted a comparative study of three powerful ensemble algorithms to determine the best predictor for the TransferIQ system:
Model	R² Score	MAE (Mean Absolute Error)
XGBoost	0.8953	€2.43 Million
Random Forest	0.9107	€2.26 Million
LightGBM	0.9339	€2.10 Million
Final Selection: LightGBM was selected as the champion model for its superior leaf-wise growth strategy, which better captured the non-linear patterns in the player valuation data.
🧠 Key Findings
Beyond Goals: The model successfully proved that social sentiment and injury history are significant drivers of market value.
Model Robustness: By addressing multicollinearity, the model remains stable and interpretable, accurately identifying the "Real" drivers of a player's price.
Valuation Accuracy: Achieved a final 
R
2
R 
2
 
 of 0.9339, indicating that the model explains over 93% of the variance in player market values.
💻 Tech Stack
Python: Primary programming language.
Machine Learning: LightGBM, Random Forest, XGBoost, Scikit-Learn.
Data Analysis: Pandas, NumPy.
Visualization: Matplotlib, Seaborn.



