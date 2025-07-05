# CI/CD Pipeline with Jenkins and Docker

This project implements a complete DevOps pipeline using **Jenkins**, **Maven**, **Docker**, **SonarQube**, and **OWASP Dependency-Check**. It automates building, analyzing, containerizing, and deploying a backend application.

---

## 🔧 Tech Stack

- Jenkins
- Maven
- Docker
- SonarQube
- OWASP Dependency Check
- GitHub

---

## SonarQube

```bash 
docker run -d -p 9000:9000 sonarqube:lts-community
```
---

## 🧩 CI Pipeline (`Jenkinsfile`)

- Clone project from GitHub
- Compile using Maven
- Run static analysis via SonarQube
- Scan dependencies for known vulnerabilities (OWASP)
- Package and Dockerize the application
- Push Docker image to Docker Hub
- Trigger downstream CD pipeline

---

## 🚀 CD Pipeline (`Jenkinsfile_cd`)

- Pull Docker image from Docker Hub
- Stop and remove existing container (if any)
- Deploy a new container

---

## 📄 Docker Run Example

```bash
docker run -d --name shopping -p 8070:8070 vasanthkarthik2703/shopping:latest
```

--- 

## Important Points

3 or more '*'(asterisk) represents secret (docker and sonarqube key).
