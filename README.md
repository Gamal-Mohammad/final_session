# Final Session – Registration App on Kubernetes

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![Apache](https://img.shields.io/badge/Apache_httpd-D22128?logo=apache&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)

> A registration-form web app, containerised and deployed to Kubernetes with rolling updates.

## Overview

Static web page containerised with **Apache httpd**. The repository is used in the DevOps training track to practise Git, building Docker images and running them as containers. `projectApp-deployment.yml` deploys it with 4 replicas using a RollingUpdate strategy.

## Tech Stack

- **Docker**
- **Kubernetes**
- **Apache httpd**
- **HTML/CSS**

## Repository Structure

```text
Dockerfile
index.html
projectApp-deployment.yml
README.md
test.txt
```

## Getting Started

### Run with Docker

```bash
git clone https://github.com/Gamal-Mohammad/final_session.git
cd final_session
docker build -t final-session .
docker run -d --name final-session -p 8080:80 final-session
```

Then open http://localhost:8080.

### Deploy to Kubernetes

| File | Kind | Name |
|---|---|---|
| `projectApp-deployment.yml` | Deployment | `projapp` |

```bash
kubectl apply -f projectApp-deployment.yml
kubectl get pods,svc
```

## Author

**Gamal Mohammad**

[![GitHub](https://img.shields.io/badge/GitHub-Gamal--Mohammad-181717?logo=github)](https://github.com/Gamal-Mohammad)
