# ☀️ Jenkins + SonarQube CI/CD Project

A fully automated CI/CD pipeline for a static website using Jenkins, Docker, and SonarQube.

## 🚀 Stack Used
- **Frontend**: HTML5, CSS3, JavaScript
- **CI/CD**: Jenkins
- **Quality Gate**: SonarQube
- **Containerization**: Docker
- **Hosting**: WSL2-based Ubuntu with SSH Deployment

## 🛠️ Pipeline Steps
1. Code pushed to GitHub triggers Jenkins via webhook
2. Jenkins pulls the code and runs SonarQube analysis
3. If quality gate passes, code is copied to target server over SSH
4. Docker image is built and run for deployment

## 🔐 SSH Setup
- Jenkins user configured with public key authentication to deployment user (`nagesh`)
- Passwordless connection enables non-interactive SSH commands

## 🐳 Docker Integration
- Jenkins builds Docker image from Dockerfile
- Runs the container for isolated deployment testing

## ⚠️ Troubleshooting Highlights
- Fixed Docker socket access: `permission denied @ /var/run/docker.sock`
- Resolved SSH `Permission denied (publickey)` by syncing `.ssh/id_rsa.pub` from Jenkins
- Solved GitHub push errors: 403 & non-fast-forward rejections

## 📎 Project Repository
[🔗 https://github.com/Nagesh241299/jenkins-sonar-project](https://github.com/Nagesh241299/jenkins-sonar-project)

## 📢 Contact
Open to DevOps collaborations and automation projects!
