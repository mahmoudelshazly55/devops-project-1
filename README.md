# 🚀 DevOps Project 1 – Dockerized Nginx with CI/CD

This is my first hands-on DevOps project where I built and automated a Dockerized Nginx application using GitHub Actions.

The project demonstrates the full DevOps flow: **code → build → CI → Docker Hub → run container**.

---

## 📌 Project Overview

* Simple static web page served using **Nginx**
* Dockerized application using **Dockerfile**
* Automated CI pipeline using **GitHub Actions**
* Image is automatically built and pushed to **Docker Hub** on every push to `main`

---

## 🛠️ Tech Stack

* Docker
* Nginx
* Git & GitHub
* GitHub Actions
* Linux (WSL / Ubuntu)

---

## 📂 Project Structure

```
.
├── Dockerfile
├── index.html
└── .github/
    └── workflows/
        └── docker-ci.yml
```

---

## ⚙️ Dockerfile

* Uses Nginx official image
* Copies `index.html` to Nginx default directory
* Exposes port 80

---

## 🔄 CI/CD Workflow (GitHub Actions)

On every push to the `main` branch:

1. Checkout the repository
2. Login to Docker Hub using GitHub Secrets
3. Build Docker image
4. Push image to Docker Hub automatically

---

## 🔐 GitHub Secrets Used

| Secret Name       | Description             |
| ----------------- | ----------------------- |
| `DOCKER_USERNAME` | Docker Hub username     |
| `DOCKER_PASSWORD` | Docker Hub access token |

---

## 🐳 Docker Image

Docker Hub Repository:

```
mahmoud999999/devops-nginx
```

---

## ▶️ How to Run the Project Locally

```bash
docker pull mahmoud999999/devops-nginx
docker run -p 8080:80 mahmoud999999/devops-nginx
```

Then open your browser:

```
http://localhost:8080
```

You should see:

```
Hello from Docker 🚀
My first DevOps project
```

---

## 🎯 What I Learned

* Writing Dockerfiles
* Working with Docker images and containers
* Using GitHub Actions for CI/CD
* Securing credentials with GitHub Secrets
* Real DevOps workflow from code to production

---

## 📈 Next Steps

* Docker Compose
* Nginx Reverse Proxy
* Kubernetes fundamentals

---

👤 **Author**: Mahmoud Elshazly

📌 Computer Science Graduate | DevOps & Cloud Enthusiast

