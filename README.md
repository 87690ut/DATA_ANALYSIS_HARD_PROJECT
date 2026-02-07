# 🚢 Titanic Survival Prediction: Machine Learning from Scratch

### 👤 **Author:** Uttam Tiwari
**Status:** ✅ Completed | **Accuracy:** ~81%

---

## 📝 Project Overview
This project is a **Binary Classification** model built using **Logistic Regression**. The goal is to predict whether a passenger on the Titanic would survive or not based on socio-economic status, age, gender, and other features.

I processed raw data, cleaned missing values, trained the model, and achieved an accuracy of approximately **81%** on the test dataset.

---

## 🛠️ Tech Stack & Libraries
The project was built using Python and the following libraries:

* **🐍 Python:** Core programming logic.
* **🐼 Pandas:** For Data Cleaning, Manipulation, and Feature Engineering.
* **🔢 NumPy:** For numerical operations.
* **📊 Seaborn & Matplotlib:** For Data Visualization (Heatmaps & Plots).
* **🤖 Scikit-Learn (sklearn):**
    * `LogisticRegression`: The core ML algorithm.
    * `train_test_split`: To separate training and testing data.
    * `confusion_matrix`: To evaluate True Positives and False Negatives.

---

## 🧠 Key Learnings & Workflow
This project was not just about coding, but understanding the **Data Science Lifecycle**:

### 1. Data Cleaning (The Hardest Part)
* **Handling Missing Values:**
    * Found that the `deck` column had too many missing values (~77%), so I **dropped** it.
    * The `age` column had missing values, which I filled using the **Median** age (to avoid outliers).
* **Dropping Irrelevant Features:**
    * Removed duplicate/redundant columns like `who`, `adult_male`, and `alive` to prevent **Data Leakage** (cheating).

### 2. Feature Encoding (Making Data "Machine-Ready")
* Machines don't understand text like "male" or "female".
* I used `.map()` to convert:
    * **Sex:** `male` → `0`, `female` → `1`
    * **Embarked:** `S` → `0`, `C` → `1`, `Q` → `2`

### 3. Model Logic (Logistic Regression)
* Used **Logistic Regression** because the target variable (`survived`) is categorical (0 or 1).
* Split the data into **80% Training** and **20% Testing** to ensure the model isn't just memorizing the answers.

---

## 📊 Model Performance
I evaluated the model using a **Confusion Matrix**.

* **Accuracy:** ~82%
* **Confusion Matrix Analysis:**
    * ✅ **True Negatives:** 123 (Correctly predicted "Died")
    * ✅ **True Positives:** 61 (Correctly predicted "Survived")
    * ❌ **False Positives/Negatives:** Only ~39 errors out of ~223 test cases.

![Confusion Matrix showing model performance with True Negatives 123, True Positives 61, False Positives and False Negatives totaling 39 errors across 223 test cases](Screenshot%202026-02-07%20104432.png)
---


## 🧪 Real-World Testing: "Jack vs Rose"
To test if the model works on custom data, I simulated the profiles of the movie characters **Jack** and **Rose**:

```python
# Simulated Data
Jack = [3rd Class, Male, Age 20, Poor]  -> Prediction: [0] (Did not Survive) 💀
Rose = [1st Class, Female, Age 17, Rich] -> Prediction: [1] (Survived) 🏆
```
---

## 👤 Author
**Uttam Tiwari**
*Aspiring Data Analyst | BCA Student*

* 💼 **LinkedIn:** [Connect on LinkedIn](https://www.linkedin.com/in/uttam-tiwari-46079a310?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)
* 📧 **Email:**  [uttamtiwari.analyst@gmail.com](mailto:[uttamtiwari.analyst@gmail.com)

---
