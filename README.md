# 🚀 React App Deployment on Kubernetes

This project demonstrates an end-to-end DevOps workflow by building, containerizing, and deploying a React application using Docker and Kubernetes.

---

## 📌 Tech Stack

* ⚛️ React.js
* 🐳 Docker
* ☸️ Kubernetes
* 🌐 Nginx

---

## 🧱 Project Overview

This project covers:

* Creating a React application
* Building optimized production files
* Containerizing the app using Docker (multi-stage build)
* Pushing the image to DockerHub
* Deploying the app on Kubernetes
* Scaling using replicas
* Exposing the application via NodePort

---

## ⚙️ Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https:/snehal11-cryto/github.com//react-k8s-app.git
cd react-k8s-app
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Run Locally

```bash
npm start
```

👉 Open: http://localhost:3000

---

### 4️⃣ Build Production App

```bash
npm run build
```

---

## 🐳 Docker Setup

### Build Docker Image

```bash
docker build -t react-k8s-app:v1 .
```

### Tag Image

```bash
docker tag react-k8s-app:v1 <your-username>/react-k8s-app:v1
```

### Push to DockerHub

```bash
docker push <your-username>/react-k8s-app:v1
```

---

## ☸️ Kubernetes Deployment (Using Commands)

### Create Deployment

```bash
kubectl create deployment react-app --image=<your-username>/react-k8s-app:v1
```

### Scale Deployment

```bash
kubectl scale deployment react-app --replicas=2
```

### Expose Service

```bash
kubectl expose deployment react-app \
--type=NodePort \
--port=80 \
--target-port=80
```

---

## 🔍 Verify Deployment

```bash
kubectl get pods
kubectl get deployments
kubectl get svc
```

---

## 🌍 Access the Application

### If using Minikube:

```bash
minikube service react-app
```

