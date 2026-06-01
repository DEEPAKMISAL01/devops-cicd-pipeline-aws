# 🚀 AWS CI/CD Pipeline with Jenkins & Docker

## 📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline using Jenkins, Docker, GitHub, and AWS EC2.

The pipeline automatically pulls source code from GitHub, builds a Docker image, and deploys the application inside a Docker container on an AWS EC2 instance.

This project was built to showcase practical DevOps skills including Continuous Integration, Continuous Deployment, containerization, automation, and cloud deployment.

---

## 🏗️ Architecture

```text
Developer
    │
    ▼
 GitHub Repository
    │
    ▼
 Jenkins Pipeline
    │
    ▼
 Docker Build
    │
    ▼
 Docker Container
    │
    ▼
 AWS EC2 Instance
```

---

## 🛠️ Tech Stack

* AWS EC2
* Jenkins
* Docker
* Git & GitHub
* Node.js
* Linux (Ubuntu)

---

## ✨ Features

* Automated CI/CD pipeline
* Source code version control using GitHub
* Jenkins pipeline automation
* Dockerized application deployment
* AWS EC2 hosting
* Automated build and deployment process
* Infrastructure-ready DevOps workflow

---

## 📂 Project Structure

```text
devops-cicd-pipeline-aws/
│
├── app.js
├── package.json
├── Dockerfile
├── Jenkinsfile
└── README.md
```

---

## 🔄 CI/CD Workflow

### Step 1: Code Commit

Developer pushes code changes to GitHub.

### Step 2: Jenkins Pipeline Trigger

Jenkins pulls the latest source code from the repository.

### Step 3: Docker Build

Docker image is built automatically from the Dockerfile.

### Step 4: Application Deployment

A Docker container is launched using the newly built image.

### Step 5: Application Access

The application becomes available through the AWS EC2 public IP.

---

## 🐳 Docker Commands Used

Build Image

```bash
docker build -t my-cicd-app .
```

Run Container

```bash
docker run -d -p 3000:3000 my-cicd-app
```

Check Running Containers

```bash
docker ps
```

View Logs

```bash
docker logs <container-id>
```

---

## ⚙️ Jenkins Pipeline Stages

### Clone Repository

Pull source code from GitHub.

### Build Docker Image

Create a Docker image using the Dockerfile.

### Run Container

Deploy the application inside a Docker container.

### Post Actions

Display pipeline success or failure status.

---

## 🚀 Deployment Steps

1. Launch AWS EC2 Instance
2. Install Docker
3. Install Jenkins
4. Configure Jenkins Pipeline
5. Connect GitHub Repository
6. Build Docker Image
7. Deploy Application Container
8. Verify Application Access

---

## 📸 Pipeline Success

The Jenkins pipeline successfully performs:

* Source Code Checkout
* Docker Image Build
* Container Deployment
* Application Availability Verification

---

## 🎯 Skills Demonstrated

* Continuous Integration (CI)
* Continuous Deployment (CD)
* Docker Containerization
* Jenkins Automation
* AWS Cloud Deployment
* Linux Administration
* Git & GitHub Workflow

---

## 🔮 Future Enhancements

* GitHub Webhook Integration
* DockerHub Image Registry
* Separate Application Server Deployment
* Nginx Reverse Proxy
* SSL/HTTPS Configuration
* Terraform Infrastructure Automation
* Prometheus Monitoring
* Grafana Dashboards

---

## 👨‍💻 Author

**Deepak Misal**

Aspiring AWS & DevOps Engineer

GitHub: https://github.com/DEEPAKMISAL01

LinkedIn: https://www.linkedin.com/in/deepakmisal/

---

## ⭐ Conclusion

This project demonstrates a complete CI/CD implementation using Jenkins, Docker, GitHub, and AWS. It highlights practical DevOps practices for automating application build and deployment workflows in a cloud environment.
