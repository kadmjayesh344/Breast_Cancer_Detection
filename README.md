# Breast_Cancer_Detection
This is my first Machine Learning project, Breast Cancer Detection, which uses patient data to classify tumors as malignant or benign. The project was built using Python, NumPy, Pandas, and Scikit-learn.
# Breast Cancer Detection using Machine Learning

## 📌 Project Overview

This is my first Machine Learning project, built using Python and Scikit-learn.

The goal of this project is to build a **binary classification model** that classifies breast tumor data into two categories:

* **Malignant (Cancerous)**
* **Benign (Non-Cancerous)**

For this project, I used the **Breast Cancer Wisconsin dataset** available through Scikit-learn and trained a **Logistic Regression** model to make predictions.

This project helped me understand the basic end-to-end workflow of a Machine Learning classification problem, from data collection and exploration to model training, evaluation, and prediction.

> **Disclaimer:** This project is for educational and learning purposes only. It is not intended to be used as a medical diagnostic system.

---

## 🛠️ Technologies Used

* **Python**
* **NumPy** – Numerical operations
* **Pandas** – Data manipulation and analysis
* **Scikit-learn** – Machine Learning and model evaluation
* **Jupyter Notebook** – Development environment

---

## 📊 Dataset

The project uses the **Breast Cancer Wisconsin Diagnostic Dataset** provided by Scikit-learn.

The dataset contains measurements computed from digitized images of breast mass cell nuclei.

The dataset includes **30 numerical features**, including measurements related to:

* Radius
* Texture
* Perimeter
* Area
* Smoothness
* Compactness
* Concavity
* Concave points
* Symmetry
* Fractal dimension

Each observation is classified into one of two target classes:

* `0` → Malignant
* `1` → Benign

---

## 🔄 Machine Learning Workflow

The project follows these steps:

### 1. Importing Dependencies

The required Python libraries and Machine Learning tools are imported using NumPy, Pandas, and Scikit-learn.

### 2. Data Collection and Processing

The Breast Cancer dataset is loaded using:

```python
sklearn.datasets.load_breast_cancer()
```

The dataset is then converted into a Pandas DataFrame for easier analysis.

### 3. Exploratory Data Analysis

The dataset is explored using:

* `.shape`
* `.info()`
* `.isnull().sum()`
* `.describe()`
* `.value_counts()`
* `.groupby()`

This helps understand the structure, statistics, class distribution, and potential missing values in the dataset.

### 4. Feature and Target Separation

The dataset is divided into:

* **X (Features):** The 30 numerical measurements
* **y (Target):** The classification label

```python
X = data_frame.drop(columns='0/1', axis=1)
y = data_frame['0/1']
```

### 5. Train-Test Split

The dataset is divided into training and testing data.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=2
)
```

* **80%** of the data is used for training.
* **20%** of the data is used for testing.

### 6. Model Training

A Logistic Regression model is created and trained using the training dataset.

```python
model = LogisticRegression()

model.fit(X_train, y_train)
```

### 7. Model Evaluation

The trained model is evaluated on both training and testing data using accuracy score.

```python
x_train_prediction = model.predict(X_train)

training_data_accuracy = accuracy_score(
    y_train,
    x_train_prediction
)
```

Testing accuracy is calculated using the same approach on unseen test data.

### 8. Prediction System

The project also includes a simple prediction system where a new set of patient measurements can be provided as input.

The input data is:

1. Converted into a NumPy array.
2. Reshaped into the required format.
3. Passed to the trained Logistic Regression model.
4. Classified as either Malignant or Benign.

```python
prediction = model.predict(input_data_reshaped)
```

---

## 💡 Key Concepts Learned

Through this project, I learned and practiced:

* Loading datasets using Scikit-learn
* Working with NumPy arrays
* Data manipulation using Pandas
* Exploratory Data Analysis
* Separating features and target variables
* Splitting data into training and testing sets
* Logistic Regression
* Model training using `.fit()`
* Generating predictions using `.predict()`
* Understanding predicted values (`ŷ`)
* Evaluating a classification model using accuracy score
* Building a basic Machine Learning prediction system

---

## 🚀 Future Improvements

I plan to improve this project by adding:

* Feature scaling using `StandardScaler`
* Confusion Matrix
* Precision, Recall, and F1-Score
* Classification Report
* ROC-AUC evaluation
* Data visualization
* Cross-validation
* Comparison with other Machine Learning algorithms
* Hyperparameter tuning
* A user-friendly web interface using Streamlit

---

## 📁 Project Structure

```text
Breast-Cancer-Detection-ML/
│
├── breast_cancer_detection.ipynb
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/breast-cancer-detection-ml.git
```

### 2. Navigate to the Project Directory

```bash
cd breast-cancer-detection-ml
```

### 3. Install the Required Libraries

```bash
pip install numpy pandas scikit-learn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook and run the cells to reproduce the project.

---

## 👨‍💻 About the Project

This project represents my **first Machine Learning project** and my first step toward gaining practical experience in Machine Learning and Artificial Intelligence.

I built this project to move beyond theoretical learning and gain hands-on experience with the complete Machine Learning workflow.

I look forward to continuously improving this project and building more complex Machine Learning projects in the future.
