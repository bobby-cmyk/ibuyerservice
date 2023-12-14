# Network Analysis and Predictive Modeling with R
### Overview
This R script is designed for comprehensive data analysis focused on network-based datasets, specifically tailored for a Bitcoin trading network. It encompasses various stages of data processing, from initial preprocessing to advanced model training and evaluation.

### Dependencies
The script relies on several R packages:

* igraph: For network analysis.
* caret: For machine learning tasks.
* ggplot2: For data visualization.
* lubridate: For handling date and time data.
* dplyr: For data manipulation.
* pROC: For Receiver Operating Characteristic (ROC) analysis.
* ROSE: For handling imbalanced data sets.
* xgboost: For executing the eXtreme Gradient Boosting algorithm.

### Script Breakdown
##### Data Preprocessing
* Loads a network dataset and formats it for analysis.
* Transforms epoch time to standard date-time format.
* Feature Selection/Engineering
* Constructs a directed graph from the dataset.
* Computes various centrality measures (in-degree, out-degree, betweenness, closeness).
* Adds these network attributes to the dataset.
* Normalizes selected features.
* Handling Imbalanced Data
* Utilizes ROSE package's ovun.sample for undersampling to balance the dataset.
##### Data Splitting
* Splits the dataset into training and testing sets.
* Configures cross-validation settings for model training.
##### Model Training
* Trains multiple models (LDA, KNN, SVM, Random Forest, Decision Tree, XGBoost, Gradient Boosting) on the training dataset.
* Stores and manages the trained models for further evaluation.
##### Model Evaluation
* Evaluates each model based on accuracy and kappa statistics.
* Generates a comparative performance metrics table.
* Testing and Performance Metrics
* Predicts using the test dataset.
* Generates confusion matrices and calculates accuracy, precision, recall, F1 score, and AUC-ROC for each model.
* Outputs a summary of test performance metrics.
##### Feature Importance Analysis
* Extracts and visualizes feature importance from the XGBoost model.
* Saves test performance metrics to a CSV file for further analysis.
