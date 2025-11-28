# Docker-Python-FlaskApp

A beginner-friendly and production-ready project that demonstrates how to containerize a simple **Flask web application** using **Docker**.  
This project is ideal for DevOps learners and engineers preparing for real-world Docker + CI/CD workflows used in MNCs.

---


## 🚀 Project Overview

This repository contains a simple **Flask web application** packaged inside a **Docker container**.  
It demonstrates key DevOps concepts:

- Containerization of applications  
- Building and managing Docker images  
- Exposing application ports  
- Running containers in isolated environments  


---


## 🧰 Tech Stack

| Component | Technology |
|----------|------------|
| Programming Language | Python 3 |
| Framework | Flask |
| Container Engine | Docker |
| Base Image | python:3.10-slim |
| OS | Linux/Windows/Mac |

---

## 📂 Repository Structure

```
flask-docker-application/
│── app.py
│── requirements.txt
│── Dockerfile
│── README.md
└── images/ (optional screenshots)
```

---


## 📦 Prerequisites

Ensure the following are installed:

- Python 3.x  
- pip  
- Docker (latest version)  

---

## 🐳 Docker Setup


### 1️⃣ Build Docker Image

```bash
docker build -t flask-docker-app .
```

### 2️⃣ Run Container

```bash
docker run -p 5000:5000 flask-docker-app
```

### 3️⃣ Access Application

```
curl localhost:5000
http://localhost:5000/
```

---


## ⚡ Automated Execution Script

To automate the process of building, running, and verifying the container, you can use the included Bash script.

**What this script does:**
1. **Builds** the Docker image tagged as \`Docker-Python-FlaskApp\`.
2. **Runs** the container in the background (detached mode) on port 5000.
3. **Waits** 20 seconds to ensure the Flask server is fully initialized.
4. **Verifies** the deployment by sending a \`curl\` request to localhost.


### Make the script executable and run it:

```
chmod +x Demo.sh
./Demo.sh
```

---

### **Browser Output**

```text
==============================
 Welcome to Dockerized Flask App
==============================

Your Python application is successfully running inside Docker 🎉
```

---


## 🔧 Useful Docker Commands

| Action | Command |
|--------|---------|
| List images | \`docker images\` |
| List containers | \`docker ps -a\` |
| Stop container | \`docker stop <name>\` |
| Remove container | \`docker rm <name>\` |
| Remove image | \`docker rmi <image_id>\` |

---

## 🛠 Troubleshooting

| Issue | Solution |
|-------|----------|
| Port already in use | Stop existing process on 5000 or change port |
| Flask not starting | Reinstall dependencies: \`pip install -r requirements.txt\` |
| Docker image too large | Use slim/buster images |
| Changes not reflected | Rebuild image: \`docker build --no-cache -t Docker-Python-FlaskApp .\` |

---

