# 📰 Fake News Detection System using NLP & Machine Learning

A machine learning–powered web application that predicts whether a news headline is **Real** or **Fake** using NLP preprocessing, TF-IDF vectorization, and a tuned classification pipeline.

---

## 🚀 Features

### 🔍 Core ML/NLP Capabilities
- Preprocessing: lowercasing, stopword removal, punctuation cleaning  
- Duplicate & empty text removal  
- Stratified train-test split  
- TF-IDF Vectorization  
- Models trained:
  - Logistic Regression  
  - Multinomial Naive Bayes  
- Hyperparameter tuning using GridSearchCV  
- Best model selection using F1-score  
- Full ML pipeline saved as `best_pipeline.joblib`  
- Metadata stored in `model_metadata.json`

### 📊 Evaluation Metrics
- Accuracy, Precision, Recall, F1-score  
- Confusion Matrix (raw & normalized)  
- ROC-AUC  
- Precision-Recall AUC  
- Threshold tuning curve  
- Top TF-IDF features for interpretability  

### 🖥️ Backend API Ready
- `/predict` → returns label + confidence  
- JSON structured responses  
- Easily integrable with any frontend (Lovable, React, Streamlit)

---

## 🏗️ System Architecture

```
User → Frontend → API → Preprocess → ML Pipeline → Prediction → Output
```
## 🏗️ System Architecture

![SmartEye System Architecture](./Figure%203.3%20Functional%20Flow%20Diagram%20of%20SmartEye%20System%20-%20visual%20selection.png)

---

## 📁 Folder Structure

```
project/
│── data/
│   ├── True.csv
│   ├── Fake.csv
│
│── model/
│   ├── best_pipeline.joblib
│   └── model_metadata.json
│
│── backend/
│   └── app.py
│
│── notebooks/
│   └── model_training.ipynb
│
└── frontend/
    └── lovable_app/
```

---

## 🔧 Installation

```
git clone <your-repo-url>
cd fake-news-detector
pip install -r requirements.txt
```

---

## ▶️ Run Backend API

```
python app.py
```

Server runs at:

```
http://127.0.0.1:5000/predict
```

---

## 🧪 API Usage Example

### Endpoint:
```
POST /predict
```

### Request:
```json
{
  "headline": "NASA confirms water on the moon surface"
}
```

### Response:
```json
{
  "prediction": "Real",
  "confidence": 0.92
}
```

---

## 📉 Model Performance Summary

| Metric | Value |
|--------|-------|
| Accuracy | ~93% |
| F1-score | Best among LR & MNB |
| ROC-AUC | High separability |

---

## 🧠 Future Enhancements
- BERT/Transformers for deep learning classification  
- Full article classification (not just headlines)  
- Fake news explainability (LIME/SHAP)  
- Continuous learning pipeline  
- Deployment via Docker + Render/AWS  

---

## 📄 License
MIT License © 2025  
