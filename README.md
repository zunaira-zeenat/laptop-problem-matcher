# 💻 Laptop Problem Matcher

A beginner-friendly **Machine Learning project using K-Nearest Neighbors (KNN)** to predict a possible laptop problem based on common symptoms.

## 📌 Project Overview

**Laptop Problem Matcher** takes common laptop symptoms as input and uses a trained KNN classification model to predict the most likely problem category.

For example:

> Slow laptop + overheating + loud fan → **Overheating**

The project demonstrates a complete basic machine-learning workflow:

**Dataset → Data Inspection → Features & Labels → Train/Test Split → KNN → Prediction → Evaluation → Gradio Interface**

---

## 🎯 Objective

The main objective of this project is to build a simple ML-based troubleshooting assistant that can identify a possible laptop problem from user-reported symptoms.

### Possible Problem Categories

* 🔥 Overheating
* 🔋 Battery Issue
* ⚡ Charging Issue
* 🖥️ Display Issue
* 📶 WiFi Issue
* 💻 Performance Issue

---

## 🧠 Machine Learning Algorithm

### K-Nearest Neighbors (KNN)

KNN is a supervised machine learning algorithm used for classification and regression.

For this project, KNN classification is used.

The model looks at the **nearest similar cases** in the training data and uses them to determine the predicted problem.

We used:

```python
KNeighborsClassifier(n_neighbors=3)
```

This means the model considers the **3 nearest neighbors** when making a prediction.

---

## 📊 Features

The model uses the following laptop symptoms:

| Feature             | Meaning                      |
| ------------------- | ---------------------------- |
| `slow`              | Laptop is running slowly     |
| `overheating`       | Laptop gets unusually hot    |
| `loud_fan`          | Laptop fan is unusually loud |
| `battery_drain`     | Battery drains quickly       |
| `frequent_crashes`  | Laptop crashes frequently    |
| `screen_flickering` | Screen flickers              |
| `wifi_problem`      | WiFi/connectivity problem    |
| `charging_problem`  | Laptop has charging problems |

The symptoms are represented as:

* `1` = Yes
* `0` = No

---

## 🔄 Project Workflow

```text
Create Dataset
      ↓
Inspect Dataset
      ↓
Create Features (X) and Label (y)
      ↓
Train/Test Split
      ↓
Create KNN Model
      ↓
Train Model
      ↓
Make Predictions
      ↓
Evaluate Model
      ↓
Create Gradio Interface
```

---

## 📈 Model Evaluation

The dataset was divided into:

* **80% training data**
* **20% testing data**

The initial model achieved:

**Accuracy: 80%**

However, this result should be interpreted carefully because the dataset used in this prototype is **synthetically generated** rather than collected from real laptop repair records.

Therefore, the 80% accuracy demonstrates the ML workflow and prototype performance, but it should **not be interpreted as real-world diagnostic accuracy**.

The project also uses:

* Accuracy
* Confusion Matrix
* Classification Report

for evaluation.

---

## 🖥️ Gradio Interface

The project includes a **Gradio-based interface** where users can select laptop symptoms using checkboxes instead of manually entering `0` and `1`.

Example:

```text
☑ Laptop is slow
☑ Laptop is overheating
☑ Fan is loud
☐ Battery drains quickly
☐ Laptop crashes frequently
☐ Screen is flickering
☐ WiFi problem
☐ Charging problem
```

The system then returns a predicted problem.

### 📸 Application Screenshot

> Add the project screenshot here.

```text
![Laptop Problem Matcher](screenshot 2026-09-16 005301.png)
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* Scikit-learn
* KNN
* Matplotlib
* Gradio
* Joblib
* Google Colab

---

## 📂 Project Structure

```text
laptop-problem-matcher/
│
├── laptop_problem_matcher.ipynb
├── app.py
├── laptop_problem_model.pkl
├── README.md
└── screenshot.png
```

---

## 🚀 How to Run

### 1. Install the required libraries

```bash
pip install pandas scikit-learn matplotlib gradio joblib
```

### 2. Train the model

Run the notebook:

```text
laptop_problem_matcher.ipynb
```

### 3. Save the trained model

The trained model is saved as:

```text
laptop_problem_model.pkl
```

### 4. Run the Gradio application

```bash
python app.py
```

The Gradio interface will open through the generated local/share link.

---

## 🧪 Example Prediction

### Input

```text
Slow: Yes
Overheating: Yes
Loud Fan: Yes
Battery Drain: No
Frequent Crashes: No
Screen Flickering: No
WiFi Problem: No
Charging Problem: No
```

### Output

```text
Predicted Problem: Overheating
```

---

## 📚 What I Learned

Through this project, I practiced:

* Creating and inspecting a dataset
* Understanding features and labels
* Splitting data into training and testing sets
* Creating a KNN classifier
* Training a machine learning model
* Making predictions
* Evaluating model accuracy
* Creating a confusion matrix
* Generating a classification report
* Saving a trained ML model
* Building a simple Gradio ML interface

---

## ⚠️ Limitations

This is an educational prototype.

The dataset is **synthetically generated**, so the model has not been validated against real laptop repair/diagnostic data.

A production-level version would require:

* A larger real-world dataset
* Expert-verified problem labels
* More detailed laptop symptoms
* Hardware/software diagnostic information
* Proper validation on unseen real-world cases

The prediction should therefore be treated as a **possible problem category**, not a definitive hardware diagnosis.

---

## 🔮 Future Improvements

Possible future improvements include:

* Collecting real laptop troubleshooting data
* Adding more problem categories
* Adding additional symptoms
* Testing different K values
* Comparing KNN with Decision Tree and Random Forest
* Improving the Gradio interface
* Adding troubleshooting suggestions for each predicted problem
* Deploying the application online

---

## 👩‍💻 Author

**Zunaira Zeenat**

Information Technology Student
Machine Learning Project

---

## ⭐ Project Highlights

**Algorithm:** K-Nearest Neighbors (KNN)

**Interface:** Gradio

**Dataset:** Synthetic laptop troubleshooting dataset

**Model Accuracy:** 80% on the current test split

**Purpose:** Educational ML troubleshooting prototype
