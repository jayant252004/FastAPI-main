# 🌟 FastAPI Continuous Delivery with GitHub Actions 🚀

## 📌 Overview
This project demonstrates Continuous Delivery by automating the creation and deployment of a Dockerized FastAPI application using GitHub Actions.

---

## 🛠️ Setup and Running Locally
### 🔹 Prerequisites
- Python 3.x installed
- `pip` package manager
- Docker installed (if running with Docker)

### 🔹 Steps
1️⃣ **Clone the repository:**
   ```sh
   git clone https://github.com/Diwish15/FastAPI
   cd FastAPI
   ```
2️⃣ **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
3️⃣ **Run the FastAPI server:**
   ```sh
   python main.py
   ```

---

## 🐳 Building and Running with Docker
### 🔹 Build Docker Image:
```sh
   docker build -t diwish345/fastapi-app:latest .
```

### 🔹 Run Docker Container:
```sh
   docker run -p 8000:8000 diwish345/fastapi-app:latest
```

---

## 🔄 GitHub Actions Workflow
### ✅ What it does:
- 🚀 Triggered on every **push** to the repository
- 🔨 Builds the Docker image
- 📤 Pushes it to **Docker Hub**

### 📝 Steps:
1️⃣ **Set up GitHub Actions Workflow** in `.github/workflows/DockerBuild.yml`
2️⃣ **Add `DOCKERTOKEN` as a GitHub Secret** (explained below)

---

## 🔑 Setting Up Docker Token
1️⃣ **Go to** [Docker Hub](https://hub.docker.com/) and log in.
2️⃣ **Navigate to** `Account Settings → Security → Access Tokens`.
3️⃣ **Generate a new token** and **add it as a secret** in GitHub:
   - Go to your GitHub repository settings
   - Navigate to `Secrets and variables → Actions → New repository secret`
   - Name it **DOCKERTOKEN** and paste the token value

---
