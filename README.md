# Electronic Health Record (EHR) System  
*A Containerized, Monitored, and Automated Healthcare Application*

---

## Overview  
This project implements a **cloud-native Electronic Health Record (EHR)** system that securely manages patient data and appointments.  
The system is built using **Node.js, MongoDB, Docker, Kubernetes, Prometheus, Grafana, Ansible, and GitHub Actions**, showcasing a full DevOps lifecycle — from CI/CD to infrastructure automation and monitoring.

---

## Features  

- **Frontend (EHR Web UI)** – Built with HTML/CSS/JS, accessible via NodePort service.  
- **Backend (Express.js API)** – Handles patient and appointment data with REST APIs.  
- **Database (MongoDB)** – Stores patient and appointment records persistently.  
- **Containerization (Docker)** – Each component runs in isolated containers.  
- **Orchestration (Kubernetes)** – Deploys and scales the application automatically.  
- **Automation (Ansible)** – Automates environment setup and deployment.  
- **CI/CD (GitHub Actions)** – Builds and pushes Docker images automatically.  
- **Monitoring (Prometheus + Grafana)** – Collects metrics and visualizes application health.

---

## Project Architecture  

![Architecture Diagram](docs/architecture.png)  
> *System flow showing how users interact with the frontend, backend, and monitoring stack.*

### Key Components
| Component | Description |
|------------|--------------|
| **Frontend Service** | User interface for patient and appointment management |
| **Backend Service** | REST API built with Express.js |
| **MongoDB Service** | Database for persistent data storage |
| **Prometheus** | Metrics collection from backend |
| **Grafana** | Visualization dashboard for monitoring |
| **Ansible** | Environment provisioning and setup |
| **GitHub Actions** | CI/CD automation for build and deploy |

---

## Tech Stack  

| Category | Technologies |
|-----------|---------------|
| **Frontend** | HTML, CSS, JavaScript |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB |
| **Containerization** | Docker |
| **Orchestration** | Kubernetes (Minikube) |
| **Monitoring** | Prometheus, Grafana |
| **Automation** | Ansible |
| **CI/CD** | GitHub Actions |
| **Version Control** | Git + GitHub |

---

## Setup and Deployment  

### 1. Clone the Repository
git clone https://github.com/🟩your-username/CA2-507-508.git
cd CA2-507-508

### 2. Build and Push Docker Images 
docker build -t madhuraaher0547/ehr-backend:latest ./backend
docker build -t madhuraaher0547/ehr-frontend:latest ./frontend
docker push madhuraaher0547/ehr-backend:latest
docker push madhuraaher0547/ehr-frontend:latest

### 3. Deploy to Kubernetes
kubectl apply -f k8s/

### 4. Deploy to Kubernetes
kubectl apply -f monitoring/

### 5. Access Services
| Service         | URL                                              |
| --------------- | ------------------------------------------------ |
| **Frontend UI** | [http://localhost:30080](http://localhost:30080) |
| **Prometheus**  | [http://localhost:30900](http://localhost:30900) |
| **Grafana**     | [http://localhost:32000](http://localhost:32000) |

### 6. Monitoring Overview
Prometheus

Collects metrics from /metrics endpoint of backend.
Target Job: ehr-backend-service.default.svc.cluster.local:5000

Grafana
Visualizes metrics such as:
CPU Usage
Memory Usage
HTTP Request Count
Uptime and Response Time

### 6. Automation
Ansible
Used to install Docker, clone repo, and run containers automatically.
ansible-playbook -i inventory.ini playbook.yml --ask-become-pass

### 6. GitHub Actions
Workflow .github/workflows/docker.yml builds and pushes Docker images to Docker Hub whenever code is pushed to main.

 

