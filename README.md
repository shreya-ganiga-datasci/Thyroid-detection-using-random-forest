# 🩺 Thyroid Detection using Random Forest

## 📌 Project Overview

This project focuses on detecting **thyroid disease** using a machine learning model based on the **Random Forest Classifier**. The dataset consists of **3163 records and 26 features**, including patient demographics and clinical test results. The model classifies patients as **hypothyroid (positive)** or **negative (normal)**.

## 📊 Dataset

* Source: `hypothyroidx.csv`
* Records: 3163
* Features: 26 (age, gender, medical test results, etc.)
* Target: `class` (0 = hypothyroid, 1 = negative)

## ⚙️ Preprocessing Steps

1. Handled missing values (replaced `?` / dropped rows).
2. Encoded categorical variables (`M/F`, `t/f`, `y/n`).
3. Converted labels (`hypothyroid` → 0, `negative` → 1).
4. Scaled numerical features using **StandardScaler**.

## 🤖 Model

* **Algorithm**: Random Forest Classifier (sklearn)
* **Train-Test Split**: 70% training, 30% testing
* **Evaluation Metrics**:

  * Accuracy: **98.7%**
  * Precision: **98.9%**
  * Recall: **99.7%**
  * F1 Score: **99.3%**

## 📈 Results

* The model achieved **high accuracy** in classifying thyroid conditions.
* Confusion matrix shows very few misclassifications.
* Feature importance analysis highlights significant clinical indicators.

## 🚀 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/thyroid-detection-rf.git
   cd thyroid-detection-rf
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run Jupyter Notebook or Colab:

   ```bash
   jupyter notebook "Thyroid detection using random forest.ipynb"
   ```

## 🔮 Prediction Demo

Custom patient inputs were tested and correctly predicted as **thyroid** or **no thyroid** cases.

Example:

```python
x_test = [72,0.6,0,0,0,0,0,0,0,0,1,30,1,0.6,1,15]
y_pred = model.predict([x_test])
print("Patient has Thyroid" if y_pred[0] == 0 else "No Thyroid")
```

