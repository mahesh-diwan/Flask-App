# 🚀 Flask CI/CD on AWS with GitHub Actions, Docker, and EC2

This project demonstrates a complete DevOps pipeline:
- Flask app containerized with Docker
- CI/CD pipeline using GitHub Actions
- Docker image pushed to Docker Hub
- Auto-deployed to AWS EC2 via SSH
- Nginx reverse proxy setup

## 📦 Tech Stack
- Flask (Python)
- Docker
- GitHub Actions (CI/CD)
- Docker Hub (image registry)
- AWS EC2 (deployment)
- Nginx (reverse proxy)

## 🛠️ Setup & Deployment

### 1. Clone this repo
```bash
git clone https://github.com/mahesh-diwan/flask-cicd.git
cd flask-cicd
```

### 2. Run locally
```bash
docker build -t flask-cicd .
docker run -p 5000:5000 flask-cicd
```

### 3. GitHub Actions (CI/CD)
On push to master, GitHub Actions will:
-Build & push Docker image to Docker Hub
-SSH into EC2 and deploy container

### 🔐 Secrets Used
-DOCKER_USERNAME
-DOCKER_PASSWORD
-EC2_HOST
-EC2_SSH_KEY

### 🌐 Live Demo
Access it here: http://<your-ec2-ip>
