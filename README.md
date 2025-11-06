# Fraud-Transaction-Detection-REST_API
Below is a **clean, professional, interview-friendly GitHub README** for your **Fraud Detection REST API** project.
You can **copy–paste this directly into your repository.**

---

#  Fraud Detection REST API

A lightweight **Machine Learning–powered REST API** built with **Flask** for predicting fraudulent financial transactions in real time.

This project demonstrates:
✅ Backend API design
✅ ML model training & integration
✅ JSON-based prediction endpoint
✅ End-to-end workflow from data → model → API

Perfect for backend, ML-assisted, or full-stack (React + API) roles.

---

# 📌 Features

✅ **Logistic Regression model** trained on credit card fraud dataset
✅ **REST API** built using Flask
✅ **Prediction endpoint** for real-time fraud detection
✅ **Model serialized** using `joblib`
✅ **Clean backend architecture**
✅ **Easy to integrate** with ReactJS or any frontend
✅ **Lightweight & deployment-ready**

---

# 🧠 Project Architecture

```
Dataset → Preprocessing → Model Training → Save Model (.sav)
               ↓
        Flask REST API
               ↓
       /predict endpoint
               ↓
   Input JSON → Output (Fraud/Not Fraud)
```

---

# 📂 Folder Structure

```
.
├── model/
│   ├── trained_model.sav
│   └── scaler.sav
├── app.py
├── requirements.txt
├── README.md
└── utils/
    ├── preprocessing.py
    └── prediction.py
```

---

# 🗂 Dataset Used

Credit Card Fraud Detection Dataset (Kaggle)

* Highly imbalanced data
* Contains anonymized features: V1, V2, … V28
* Binary classification:

  * `0` → Legitimate
  * `1` → Fraud

---

# 🔧 Tech Stack

### Backend

* **Python 3.x**
* **Flask**
* **Joblib** for model loading
* **NumPy** / **Pandas**

### Machine Learning

* **Logistic Regression**
* **Scikit-learn**
* **StandardScaler**

---

# 🚀 How to Run the Project Locally

### ✅ 1. Clone the repository

```bash
git clone https://github.com/your-username/REST_API_for_fraud-detection.git
cd REST_API_for_fraud-detection
```

### ✅ 2. Create virtual environment

```bash
python -m venv venv
source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows
```

### ✅ 3. Install dependencies

```bash
pip install -r requirements.txt
```

### ✅ 4. Run the API

```bash
python app.py
```

API will start on:
👉 **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

---

# 📡 API Endpoints

## ✅ **POST /predict**

Predicts whether a transaction is fraudulent.

### **Request Format**

```json
{
  "V1": -1.23,
  "V2": 0.45,
  "V3": -2.13,
  "...": "...",
  "Amount": 149.99
}
```

### **Response Format**

```json
{
  "fraud_prediction": 0,
  "message": "Transaction is legitimate."
}
```

OR

```json
{
  "fraud_prediction": 1,
  "message": "Fraudulent transaction detected!"
}
```

---

# 🤖 Machine Learning Workflow

### ✅ 1. Preprocessing

* Standard scaling
* Handling imbalanced dataset
* Train-test split

### ✅ 2. Model Training

* Logistic Regression
* Selected for being fast, interpretable & effective
* Optimized with class weights

### ✅ 3. Model Export

```python
joblib.dump(model, "trained_model.sav")
```

### ✅ 4. API Integration

Model loaded once at startup for faster prediction:

```python
model = joblib.load("model/trained_model.sav")
```

---

# 💡 Why Logistic Regression?

✅ Fast
✅ Works well with imbalanced data
✅ High interpretability
✅ Low resource usage → good for backend APIs

---

# 🌐 Deployment Options

This API can be deployed on:

✅ **Render**
✅ **Railway.app**
✅ **Azure App Service**
✅ **AWS Elastic Beanstalk**
✅ **Google Cloud Run**
✅ **Docker containers**

Deployment-ready with minimal changes.

---

# 🔥 Future Improvements

✅ Add authentication (JWT)
✅ Add request validation layer
✅ Add rate limiting
✅ Add logging & monitoring
✅ Build frontend dashboard using ReactJS
✅ Deploy with Docker + CI/CD

---

# 📘 Use Cases

* Financial fraud detection
* Payment gateway validation
* Banking risk scoring
* Real-time transaction monitoring
* ML model serving for FinTech

---

# 👨‍💻 Author

**Karan Raj**
Backend Developer | NIT Agartala
