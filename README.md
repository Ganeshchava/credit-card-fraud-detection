# Credit Card Fraud Detection

## Task Objectives

The goal of this project is to develop a machine learning model that can predict fraudulent credit card transactions. The dataset consists of various transaction details, including the transaction amount, user ID, merchant information, timestamps, etc. The model should minimize false positives and maximize fraud detection accuracy.

## Steps to Run the Project

### 1. Clone the repository
```bash
git clone https://github.com/Ganeshchava/credit-card-fraud-detection.git
cd credit-card-fraud-detection
```
### 2. Install Dependencies

Make sure you have Python installed. Then install the required libraries:

```bash
pip install -r requirements.txt
```
### 3. Run the Project
If you are using Google Colab:
- Open FraudDetection.ipynb in Google Colab.

- Upload the dataset fraudTrain.csv.

- Run the cells one by one to explore preprocessing, training, and evaluation steps.
### If you're using Jupyter Notebook locally:
```bash
jupyter notebook FraudDetection.ipynb
```
## Project Workflow & Detailed Explanation
### 1. Data Loading and Exploration
- Loaded the dataset using pandas, and previewed the first few records.

- Checked for missing values and cleaned unnecessary columns.

- Explored distributions of key variables like amount, category, merchant, and gender.

### 2. Data Preprocessing
Split the dataset into features (X) and target (y where is_fraud = 1).

- Numerical features: like amt, lat, long, etc.

- Categorical features: like category, gender, merchant, city, etc.

- Applied preprocessing using ColumnTransformer:

- Numerical: missing value imputation + standard scaling.

- Categorical: mode imputation + ordinal encoding (to convert to numeric).

### 3. Model Building
Used a Random Forest Classifier:

- Good performance on tabular data.

- Robust to outliers and handles both types of features.

- Built a pipeline combining preprocessing + classifier.

- Trained the model on the cleaned dataset.

### 4. Model Evaluation
Evaluated using:


- Confusion Matrix: to see true vs. predicted labels.

- Classification Report: Precision, Recall, F1-score.

- ROC Curve & AUC Score: for visual performance comparison.


###  5. Results

The model performed well with:

- High Precision and Recall for the fraud class (1).

- Strong ROC-AUC score indicating good class separation.

- SHAP Summary Plot highlighted:

- amount, category, and merchant as key indicators of fraud.

- The model was able to detect fraud effectively while minimizing false alarms.
