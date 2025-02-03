# credit-card-fraud-detection
Objectives
Data Collection and Preprocessing:

Collect a dataset of credit card transactions, including both fraudulent and non-fraudulent transactions.
Clean and preprocess the data to handle missing values, outliers, and any inconsistencies.
Perform feature engineering to create meaningful features that can help in distinguishing between fraudulent and legitimate transactions.
Exploratory Data Analysis (EDA):

Analyze the dataset to understand the distribution of transactions and identify patterns or anomalies.
Visualize the data to gain insights into the characteristics of fraudulent transactions compared to legitimate ones.
Model Development:

Split the data into training and testing sets.
Develop various machine learning models (e.g., Logistic Regression, Decision Trees, Random Forest, Gradient Boosting, Neural Networks) to predict fraudulent transactions.
Perform hyperparameter tuning to optimize the performance of the models.
Model Evaluation:

Evaluate the performance of the models using appropriate metrics such as accuracy, precision, recall, F1-score, and the Area Under the Receiver Operating Characteristic Curve (AUC-ROC).
Compare the performance of different models and select the best-performing model for deployment.
Deployment and Monitoring:

Deploy the selected model in a real-time environment to monitor incoming transactions.
Implement a feedback loop to continuously update and improve the model based on new data and detected fraud patterns.
Challenges
Imbalanced Data: Fraudulent transactions are typically much fewer than legitimate ones, leading to an imbalanced dataset. Techniques such as resampling, SMOTE (Synthetic Minority Over-sampling Technique), or anomaly detection methods might be needed.
Feature Selection: Identifying the most relevant features that contribute to distinguishing between fraudulent and non-fraudulent transactions.
Real-time Processing: Ensuring the system can handle and analyze transactions in real-time without significant latency.
Evolving Fraud Patterns: Fraudsters continuously evolve their techniques, so the model needs to adapt and stay current with new fraud patterns.
Deliverables
A cleaned and preprocessed dataset ready for analysis.
A comprehensive report on exploratory data analysis with visualizations.
Trained machine learning models with performance metrics and evaluation results.
A deployed fraud detection system capable of real-time transaction analysis.
Documentation detailing the methodology, model development process, and deployment strategy.
Success Criteria
The detection system should achieve a high recall rate to minimize false negatives (i.e., missed fraudulent transactions).
The system should maintain a low false positive rate to avoid flagging legitimate transactions incorrectly.
The model should be able to process transactions in real-time, with minimal delay.
Continuous improvement and adaptation of the model to detect new fraud patterns effectively.

TransactionID: A unique identifier for each transaction.
Timestamp: The date and time when the transaction occurred.
CardNumber: A partially masked card number or unique card identifier.
TransactionAmount: The amount of the transaction.
MerchantID: A unique identifier for the merchant where the transaction took place.
Location: The geographic location of the transaction (could be split into city, state, country).
TransactionType: Type of transaction (e.g., purchase, cash withdrawal, online payment).
PreviousTransactionInterval: Time since the last transaction on the same card.
DailyTransactionCount: Number of transactions made by the cardholder in the last 24 hours.
DailyTransactionAmount: Total amount spent by the cardholder in the last 24 hours.
AvgTransactionAmount: Average amount spent per transaction over a specified period.
FraudFlag: A binary indicator (0 or 1) denoting whether the transaction is fraudulent (1) or not (0).
DeviceID: Identifier for the device used in the transaction.
IP Address: The IP address from which the transaction was initiated.
Browser Information: Information about the browser used for the transaction.
DistanceFromHome: The geographic distance between the transaction location and the cardholder's home location.
DistanceFromLastTransaction: The distance from the previous transaction location.
IsForeignTransaction: Indicator of whether the transaction was made in a foreign country.
IsHighRiskCountry: Indicator of whether the transaction occurred in a high-risk country.
IsProxyUsed: Indicator of whether a proxy was used during the transaction.

Power BI Dashboard - Transaction Analysis

Page 1: Overview Dashboard
Top Row:

Card Visuals:
Sum of TransactionAmount
Sum of AvgTransactionAmount
Sum of FraudFlag
Middle Row:

KPI Chart: Sum of TransactionAmount and AvgTransactionAmount by TransactionType
Pie Chart: Sum of FraudFlag
Line Chart: Sum of TransactionAmount and FraudFlag by Year
Bottom Row:

Map Chart: Sum of TransactionAmount and FraudFlag by Location
Line Chart: Count of TransactionType by FraudFlag
Stacked Bar Chart: Sum of FraudFlag by Timestamp
Page 2: Transaction Amount by Transaction ID
Stacked Column Chart: Sum of TransactionAmount by TransactionID
Page 3: Fraud Analysis
Donut Chart: Sum of TransactionAmount by FraudFlag
Page 4: Transaction Trends Over Time
Line Chart: Sum of FraudFlag and Sum of TransactionAmount by Timestamp
Page 5: Fraud Pattern Visualization
Tree Map: Sum of TransactionAmount and Timestamp by FraudFlag
Page 6: Previous Transaction Interval Analysis
Clustered Column Chart: Sum of TransactionAmount by PreviousTransactionInterval
