# Credit Card Fraud Detection using ETL Process and Machine Learning
📌 Project Overview

This project is a Credit Card Fraud Detection System developed using Python, ETL Process, and Machine Learning techniques.
The system analyzes credit card transaction data and predicts whether a transaction is fraudulent or non-fraudulent using the Logistic Regression Algorithm.

The project demonstrates:

ETL (Extract, Transform, Load) Process
Data Preprocessing
Data Visualization
Machine Learning Model Training
Fraud Detection Analysis
Result Evaluation using Confusion Matrix and Classification Report

The implementation is done using Python libraries such as:

Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn

🎯 Objectives
To detect fraudulent credit card transactions
To understand the ETL process in Data Mining
To apply Machine Learning algorithms on real-world datasets
To improve transaction security
To analyze fraud transaction patterns
🔄 ETL Process Used in Project
1️⃣ Extract

The dataset is extracted from a CSV file using the Pandas library.

data = pd.read_csv('creditcard.csv')

The dataset contains:

Transaction details
Transaction amount
Time
Fraud labels

2️⃣ Transform

The transformation process includes:

Checking dataset information
Checking missing values
Data preprocessing
Feature scaling
Splitting dataset into training and testing data
Checking Missing Values
data.isnull().sum()
Feature Scaling
scaler = StandardScaler()
data['Amount'] = scaler.fit_transform(data[['Amount']])

3️⃣ Load

The transformed data is loaded into the Logistic Regression machine learning model for training and prediction.

model.fit(X_train, y_train)

The trained model predicts whether transactions are fraud or non-fraud.

🛠️ Technologies Used
Technology	Purpose
Python	Programming Language
Pandas	Data Handling
NumPy	Numerical Operations
Matplotlib	Data Visualization
Seaborn	Graph Plotting
Scikit-learn	Machine Learning
📂 Dataset Information

The project uses the Credit Card Fraud Detection Dataset.

Dataset Features:
284,807 transaction records
31 columns
Features from V1 to V28
Amount column
Class column
Class Labels:
0 → Non-Fraud Transaction
1 → Fraud Transaction

⚙️ System Requirements
Hardware Requirements
Processor: Intel i3 or above
RAM: 4GB minimum
Storage: 1GB free space
Software Requirements
Python 3.x
Jupyter Notebook / VS Code
Required Python Libraries
📊 Data Visualization

The project visualizes fraud and non-fraud transactions using a count plot.

sns.countplot(x='Class', data=data)
plt.title("Fraud vs Non-Fraud Transactions")
plt.show()

This graph helps understand transaction distribution.

🤖 Machine Learning Model
Logistic Regression Algorithm

The Logistic Regression algorithm is used to classify transactions as:

Fraudulent
Non-Fraudulent
Model Training
model = LogisticRegression(max_iter=10000)
model.fit(X_train, y_train)

📈 Model Evaluation

The model is evaluated using:

Classification Report
Precision
Recall
F1-Score
Confusion Matrix
Prediction
y_pred = model.predict(X_test)
Classification Report
print(classification_report(y_test, y_pred))

📉 Confusion Matrix

The confusion matrix helps visualize:

Correct predictions
Incorrect predictions
Fraud detection accuracy
sns.heatmap(confusion_matrix(y_test, y_pred), annot=True, fmt='d')

✅ Advantages
Fast fraud detection
Improves banking security
Reduces financial losses
Detects suspicious transactions
Supports real-time analysis
❌ Limitations
Requires a large dataset
Accuracy depends on training data
Logistic Regression has limitations for highly complex fraud patterns
🔮 Future Scope
Use Deep Learning algorithms
Real-time fraud monitoring system
Web-based fraud detection dashboard
Integration with banking applications
Cloud-based fraud detection system
▶️ How to Run the Project
Step 1: Install Python Libraries
pip install pandas numpy matplotlib seaborn scikit-learn
Step 2: Add Dataset

Place the dataset file in the project folder:

creditcard.csv
Step 3: Run the Program
python fraud_detection.py
📷 Sample Outputs

The project generates:

Fraud vs Non-Fraud Graph
Classification Report
Confusion Matrix Heatmap

These outputs help evaluate the fraud detection model.

📚 References
Python Official Documentation
Scikit-learn Documentation
Pandas Documentation
Kaggle Credit Card Fraud Detection Dataset
