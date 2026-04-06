### Network Security Project for Phishing Data

# 🔐 End-to-End MLOps Network Security System (Phishing Detection)

## 🚀 Project Overview

This project is an **end-to-end MLOps pipeline** designed to detect phishing attacks in network data. It automates the complete machine learning lifecycle — from data ingestion to deployment — using modern cloud and DevOps practices.

The system is built to simulate a **real-world production ML system** with scalability, automation, and deployment capabilities.

---

## 🎯 Problem Statement

Cybersecurity threats, especially phishing attacks, are rapidly increasing. Traditional rule-based systems fail to detect evolving threats.

This project solves the problem by building an **automated, scalable, and deployable ML system** that:

* Ingests network data
* Processes and validates it
* Trains machine learning models
* Deploys the model as an API
* Enables real-time predictions

---

## 🧠 Solution Approach

The solution follows a complete **MLOps lifecycle**:

```
Data → ETL → Validation → Transformation → Model Training → Deployment → Prediction API
```

---

## 🏗️ Architecture

### 🔹 High-Level Flow

```
Local Code → Docker → AWS ECR → EC2 → FastAPI → User Requests
```

### 🔹 CI/CD Flow

```
GitHub Push → GitHub Actions → Build Docker Image → Push to ECR → Deploy on EC2
```

---

## ⚙️ Tech Stack

### 💻 Programming & Frameworks

* Python
* FastAPI

### 📊 Machine Learning

* Scikit-learn
* Pandas
* NumPy

### 🗄️ Database

* MongoDB Atlas

### ⚙️ MLOps & DevOps

* Docker
* GitHub Actions (CI/CD)

### ☁️ Cloud (AWS)

* EC2 (Compute)
* ECR (Docker Registry)
* S3 (Optional Storage)

---

## 📂 Project Structure

```
networksecurity/
│
├── components/
├── pipeline/
├── entity/
├── utils/
│
├── app.py
├── main.py
├── Dockerfile
├── setup.py
├── README.md
```

---

## 🔄 MLOps Pipeline

### 1️⃣ Data Ingestion

* Reads phishing dataset
* Converts CSV → JSON
* Stores data in MongoDB

### 2️⃣ Data Validation

* Schema validation
* Data quality checks

### 3️⃣ Data Transformation

* Feature engineering
* Preprocessing pipeline

### 4️⃣ Model Training

* Trains ML model
* Saves model & preprocessor

### 5️⃣ Deployment

* Docker containerization
* CI/CD pipeline with GitHub Actions
* Deployment to AWS EC2

---

## 🌐 API Endpoints

### 🔹 Train Model

```
GET /train
```

### 🔹 Predict

```
POST /predict
```

* Upload CSV file
* Returns predictions

---

## 🐳 Docker Usage

### Build Image

```
docker build -t networksecurity .
```

### Run Container

```
docker run -d -p 8000:8000 networksecurity
```

---

## ☁️ AWS Deployment

### Steps:

1. Push Docker image to AWS ECR
2. Launch EC2 instance (t2.micro)
3. Pull image from ECR
4. Run container on EC2
5. Access API via public IP

---

## 🔁 CI/CD Pipeline

* Triggered on GitHub push
* Builds Docker image
* Pushes to ECR
* Deploys on EC2 using self-hosted runner

---

## 📊 Features

✔ End-to-end ML pipeline
✔ Automated training
✔ Real-time prediction API
✔ Dockerized deployment
✔ CI/CD automation
✔ Cloud deployment (AWS)
✔ Modular code structure

---

## 💡 Key Learnings

* MLOps lifecycle implementation
* Docker containerization
* CI/CD pipeline automation
* AWS deployment (EC2, ECR)
* API-based ML serving

---

## 🚀 Future Improvements

* Add MLflow for experiment tracking
* Implement model monitoring
* Add real-time streaming (Kafka)
* Build frontend dashboard
* Add authentication to APIs

---

## 📌 Conclusion

This project demonstrates how to build and deploy a **production-ready ML system** using MLOps principles. It integrates machine learning, backend development, and cloud deployment into a single scalable pipeline.
