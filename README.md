💳 Credit Card Fraud Detection
📌 Project Overview
This project focuses on building a machine learning model to detect fraudulent credit card transactions. Fraud detection is a critical application of AI in the financial sector, where the goal is to identify unauthorized transactions in real-time to minimize financial loss for both banks and customers.
🧠 The Challenge: Class ImbalanceThe primary difficulty in fraud detection is the extreme class imbalance. In standard datasets, legitimate transactions often outweigh fraudulent ones by 99.9% to 0.1%. A model that simply predicts "Not Fraud" for every case would have 99.9% accuracy but would be completely useless. This project explores techniques like SMOTE, Random Undersampling, and specialized evaluation metrics to overcome this.📊 Dataset InformationSource: Kaggle Credit Card Fraud Detection DatasetTransactions: 284,807Features: 30 (Time, Amount, and V1-V28 PCA-transformed features)Target: Class (1 for Fraud, 0 for Legitimate)
🛠️ Tech StackLanguage: PythonLibraries:
Pandas & NumPy: Data manipulationMatplotlib & Seaborn:
Exploratory Data Analysis (EDA)Scikit-Learn: Model building and evaluationImbalanced-learn (imblearn): Handling class imbalance
🚀 Project PipelineExploratory Data Analysis (EDA): Visualizing transaction distributions and correlations.
Data Preprocessing: Scaling the Amount and Time features using StandardScaler.
Handling Imbalance: Comparing SMOTE (Synthetic Minority Over-sampling Technique) vs. NearMiss (Undersampling).
Model Selection: Training and Testing:Random Forest Classifier
Evaluation: Moving beyond accuracy to focus on Precision-Recall Curves, AUPRC, and F1-Score.
📈 Results & EvaluationSince this is an imbalanced problem, we focus on the Recall (how many frauds did we catch?) and Precision (how many of our "fraud" flags were actually correct?).
ModelPrecisionRecallF1-ScoreAUC-ROC
Random Forest0.950.820.880.94
