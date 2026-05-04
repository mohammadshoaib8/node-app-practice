# 🚀 End-to-End CI/CD Pipeline with Docker, Nginx & GitHub Actions

![CI/CD](https://img.shields.io/badge/CI/CD-Automated-blue)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![Nginx](https://img.shields.io/badge/Nginx-ReverseProxy-green)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-black)

---

## 📌 Project Overview

This project demonstrates a **complete CI/CD pipeline** using:

- 🐳 Docker (Containerization)
- 🌐 Nginx (Reverse Proxy)
- ☁️ AWS EC2 (Deployment)
- ⚙️ GitHub Actions (Automation)

👉 The application is automatically built, pushed, and deployed whenever code is pushed to GitHub.

---

##  Architecture

Developer → GitHub → GitHub Actions → Docker Hub → EC2 → Nginx → App 🚀
---

## 🛠️ Tech Stack

| Tool            | Purpose                          |
|-----------------|----------------------------------|
| Node.js         | Backend Application              |
| Docker          | Containerization                 |
| Nginx           | Reverse Proxy                    |
| AWS EC2         | Hosting Server                   |
| GitHub Actions  | CI/CD Automation                 |
| Docker Hub      | Image Registry                   |

---

## 📂 Project Structure

├── app.js
├── package.json
├── Dockerfile
└── .github/
  └── workflows/
     └── deploy.yml

---

## ⚙️ Setup Instructions

### 🔹 1. Clone Repository

```bash
git clone https://github.com/your-username/node-app-practice.git
cd node-app-practice

🔹 2. Build Docker Image
docker build -t my-node-app .

🔹 3. Run Container
docker run -d -p 3000:3000 my-node-app

🔹 4. Setup EC2 Server
Launch Ubuntu EC2
Open ports: 22, 80, 3000

🔹 5. Install Docker on EC2
sudo apt update
sudo apt install docker.io -y

🔹 6. Configure Nginx
server {
    listen 80;

    location / {
        proxy_pass http://localhost:3000;
    }
}

🔹 7. Restart Nginx
sudo systemctl restart nginx

🔐 GitHub Secrets Used
Secret Name	Description
DOCKER_USERNAME	Docker Hub Username
DOCKER_PASSWORD	Docker Hub Token
EC2_HOST	EC2 Public IP
EC2_USER	SSH Username
EC2_SSH_KEY	Private Key (.pem)

🔄 CI/CD Workflow
Code Push
   ↓
GitHub Actions Triggered
   ↓
Docker Image Build
   ↓
Push to Docker Hub
   ↓
SSH into EC2
   ↓
Pull Latest Image
   ↓
Restart Container 🚀


📸 Output

👉 Access application via:

http://<EC2-PUBLIC-IP>

🙌 Author

👤 Mohammad Shoaib
💼 AWS and DevOps Engineer
## 🙌 Connect with me

🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/mohammadshoaib8/)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohammad%20Shoaib-blue?logo=linkedin&style=for-the-badge)](https://www.linkedin.com/in/mohammadshoaib8/)
