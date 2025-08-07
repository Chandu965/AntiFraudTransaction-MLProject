AntiFraudTransactions - Fraud Detection using Machine Learning
This project focuses on detecting fraudulent transactions using machine learning techniques on a large-scale financial dataset. The goal is to build a predictive model that can effectively identify potentially fraudulent transactions, thus assisting financial institutions in minimizing fraud risk.
⚡ Optimization with Vaex & Incremental Predictors
To efficiently process and train on large-scale datasets (~6M+ records), we leveraged the following:

🔹 Vaex – Out-of-Core DataFrames for Big Data
Vaex is a high-performance Python library for lazy, memory-efficient data processing of large datasets. Instead of loading all data into memory like Pandas, Vaex uses zero-copy memory mapping, allowing you to:

-> Load massive datasets quickly without RAM overflow

-> Perform fast filtering, grouping, joins, and aggregations

-> Utilize lazy evaluation for optimized computations

In this project, Vaex was used to preprocess the large dataset efficiently, enabling smooth feature engineering and transformation even on limited hardware.

🔹 Incremental Predictors – Handling Data in Chunks
Incremental learning, also known as online learning, allows machine learning models to be trained on data that arrives in chunks rather than all at once.

In our case:

-> Instead of training the model on the entire dataset at once (which is resource-heavy), we trained using batches.

-> This approach uses models that support .partial_fit() (like SGDClassifier, PassiveAggressiveClassifier from scikit-learn).

Benefits:

  -> Reduced memory usage

  -> Real-time learning support

  -> Adaptable to streaming data scenarios

This was crucial for working with limited memory and scaling the training pipeline effectively without compromising performance.

⚙️ Key Features
  -> Data cleaning, EDA, and feature engineering

  -> Class imbalance handling using RandomUnderSampler and SMOTE

  -> Multiple model evaluation (Logistic Regression, Random Forest, XGBoost)

  -> Achieved up to 89% accuracy

  -> Model interpretability using feature importance plots
