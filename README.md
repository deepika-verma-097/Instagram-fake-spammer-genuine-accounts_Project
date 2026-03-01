# Instagram-fake-spammer-genuine-accounts_Project
Fakes and spammers are a major problem on all social media platforms, including Instagram. Detecting them using machine learning. In this dataset fake and spammer are interchangeable terms.

---

## 📖 Overview

Fake and spam accounts are a major issue on Instagram.  
This project builds Machine Learning and Deep Learning models to classify Instagram accounts as Fake or Genuine using structured profile features.

---

## 🎯 Objective

To develop a predictive model capable of accurately detecting fake Instagram accounts using supervised learning techniques.

---

## 📊 Dataset Summary

- Training Records: 576  
- Test Records: 120  
- Features: 11  
- Target Variable: fake (1 = Fake, 0 = Genuine)  

Dataset collected via web crawler (March 2019).

---

## 🔍 Exploratory Data Analysis

Performed:

- Count Plot (Fake vs Genuine)
- Correlation Heatmap
- Boxplots (Followers & Posts)
- Histogram Distribution
- Scatter Matrix

Key Findings:
- Fake accounts often lack profile pictures.
- Username numeric patterns correlate with fake accounts.
- Followers distribution highly skewed.

---

## 🤖 Models Implemented

### 1️⃣ Decision Tree
Accuracy: ~87%

### 2️⃣ Random Forest
Used for feature importance analysis.

### 3️⃣ Artificial Neural Network (ANN)

Architecture:
- Dense(50) + Dropout(0.3)
- Dense(150) + Dropout(0.3)
- Dense(25) + Dropout(0.3)
- Output Layer (Softmax)

Optimizer: Adam  
Loss: Categorical Crossentropy  
Epochs: 20  

---

## 📈 Model Performance

ANN achieved:

- Accuracy: ~95%
- Correct Predictions: 106 / 120
- Balanced Precision & Recall

---

## 💾 Model Files

models/
- decision_tree_model.pkl
- random_forest_model.pkl
- ann_model.keras

---

## Dashboard

![Dashboard Preview](https://github.com/deepika-verma-097/Instagram-fake-spammer-genuine-accounts_Project/blob/main/snapshot_of%20_dashboard.png)

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras

---

## 🚀 Future Improvements

- Hyperparameter tuning
- XGBoost implementation
- Web app deployment
- Real-time API integration

---

## 👩‍💻 Author

Deepika Verma  
Machine Learning & Data Analytics Enthusiast
