# 🌲 Forest Cover Type Prediction using Machine Learning

## 📌 Project Overview

This project applies **Machine Learning techniques to predict forest cover types** using environmental data.
The goal is to analyze geographical and environmental features and build a model that predicts the **type of forest cover** present in a specific area.

The project demonstrates how **data preprocessing, feature scaling, model training, and evaluation** are used in a real-world machine learning workflow.

---

## 🎯 Project Objectives

* Load and analyze a forest dataset
* Perform **data exploration and preprocessing**
* Split the dataset into training and testing data
* Train a **Machine Learning model**
* Evaluate the model using regression metrics
* Visualize the distribution of forest cover types

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📂 Project Structure

```
Edunet-Project
│
├── Forest_Fire_Prediction.ipynb
├── README.md
└── requirements.txt
```

### File Description

**Forest_Fire_Prediction.ipynb**

Main notebook containing:

* Data loading
* Data preprocessing
* Feature scaling
* Model training
* Model evaluation
* Visualization

---

## ⚙ Installation

Clone the repository:

```
git clone https://github.com/palrithika29/Edunet-Project.git
```

Move into the project directory:

```
cd Edunet-Project
```

Install required libraries:

```
pip install -r requirements.txt
```

---

## ▶ How to Run the Project

1. Install the required libraries.
2. Open Jupyter Notebook.

```
jupyter notebook
```

3. Run the notebook:

```
Forest_Fire_Prediction.ipynb
```

---

## 🔬 Machine Learning Workflow

### 1️⃣ Data Loading

The dataset is loaded using Pandas:

```python
df = pd.read_csv("dataset.csv")
```

---

### 2️⃣ Data Exploration

The dataset is explored using:

* `df.head()`
* `df.info()`
* `df.describe()`
* Missing value checks

---

### 3️⃣ Data Visualization

A histogram is created to visualize the distribution of **forest cover types**.

```python
sns.histplot(df["Cover_Type"])
```

---

### 4️⃣ Feature Selection

The **Aspect column is removed** as it is not required for prediction.

```python
df.drop(columns=["Aspect"], inplace=True)
```

---

### 5️⃣ Feature and Target Variables

The dataset is divided into:

* **X (Features)** – Environmental variables
* **Y (Target)** – Forest cover type

```python
x = df.drop(columns=["Cover_Type"])
y = df["Cover_Type"]
```

---

### 6️⃣ Train-Test Split

The dataset is split into:

* **80% training data**
* **20% testing data**

```python
train_test_split(test_size=0.2, random_state=42)
```

---

### 7️⃣ Feature Scaling

Standardization is applied using **StandardScaler** to improve model performance.

```python
StandardScaler()
```

---

### 8️⃣ Model Training

A **Linear Regression model** is trained using the scaled training data.

```python
model = LinearRegression()
model.fit(xtrain, ytrain)
```

---

### 9️⃣ Model Prediction

Predictions are made on the test dataset.

```python
ypred = model.predict(xtest)
```

---

### 🔟 Model Evaluation

The model is evaluated using the following metrics:

* **Mean Absolute Error (MAE)**
* **Mean Squared Error (MSE)**
* **R² Score**

Results obtained:

```
Mean Absolute Error: 0.7225
Mean Squared Error: 1.3258
R-squared Score: 0.3172
```

These metrics help measure how accurately the model predicts forest cover types.

---

## 📊 Visualization

The project includes graphical visualization using **Matplotlib and Seaborn** to understand the distribution of forest cover types in the dataset.

---

## 👩‍💻 Contributors

-**Rithika Ramashankar Pal**
-**Anchal Kamlesh Yadav**

---

## 📚 Learning Outcomes

Through this project we learned:

* Data preprocessing using Pandas
* Data visualization using Seaborn and Matplotlib
* Feature scaling using StandardScaler
* Machine learning model training using Scikit-learn
* Model evaluation using regression metrics

---

## 🚀 Future Improvements

Possible improvements for this project include:

* Using **classification models instead of regression**
* Applying **Random Forest or Decision Tree models**
* Improving model accuracy through **feature engineering**
* Creating a **web interface for predictions**

---

⭐ This project demonstrates the application of **machine learning techniques to environmental data analysis and prediction.**
