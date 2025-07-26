# 🌐 Full Stack DevOps Project Collection 🚀

Welcome to the **DevOps + WebApp Projects Repository**! This repo contains four exciting and practical web applications, each designed using different frameworks and deployed using modern DevOps practices.

---

## 📁 Projects Overview

### 1. 📊 Expenses Tracker WebApp (`Expenses-Tracker-WebApp`)
A full-stack web application to track personal expenses with an interactive UI and secure backend.

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js / Express.js
- **Database:** MongoDB
- **Features:** User authentication, category-wise expense tracking, analytics
- **Deployment:** Docker, Nginx, GitHub Actions

---

### 2. 📝 Django Notes App (`django-notes-app`)
A minimalist and powerful note-taking application built with Django.

- **Framework:** Django
- **Database:** SQLite / PostgreSQL
- **Features:** Create, edit, delete notes; user login system
- **DevOps Stack:** Docker, Gunicorn, Nginx, GitHub CI/CD
- **Bonus:** Admin panel for managing content

---

### 3. 🐍 Flask App for ECS (`flask-app-ecs`)
A simple Flask API project designed to demonstrate containerization and deployment on **Amazon ECS (Fargate)**.

- **Framework:** Flask
- **Use Case:** RESTful API for demo/test
- **Deployment:** Docker + ECS + ECR + Load Balancer
- **Monitoring:** CloudWatch Logs

---

### 4. 🏗️ Two-Tier Flask App (`two-tier-flask-app`)
A cloud-native **2-tier application**: Flask frontend with MySQL backend, great for understanding scalable architectures.

- **Architecture:** 2-tier (App + DB)
- **Backend:** Flask
- **Database:** MySQL (Dockerized or RDS)
- **DevOps Tools:** Docker Compose, Nginx, Terraform (optional)
- **Purpose:** Ideal for demoing CI/CD, DB migrations, and service scaling

---

## 🛠 DevOps Highlights

✅ Dockerized Microservices  
✅ Nginx as Reverse Proxy  
✅ CI/CD with GitHub Actions  
✅ ECS & EC2 Deployments  
✅ Monitoring via CloudWatch  
✅ Infrastructure as Code (IaC) - Terraform

---

## 🚀 How to Run

```bash
# Clone this repository
git clone https://github.com/Prasadk1618/Projects.git
cd projects

# Go to any project directory
cd Expenses-Tracker-WebApp

# Build and run the app (example with Docker Compose)
docker compose up --build
