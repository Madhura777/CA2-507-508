# 🏥 Electronic Health Record (EHR) System  
*A Containerized, Monitored, and Automated Healthcare Application*

---

## 📖 Overview  
This project implements a **cloud-native Electronic Health Record (EHR)** system that securely manages patient data and appointments.  
The system is built using **Node.js, MongoDB, Docker, Kubernetes, Prometheus, Grafana, Ansible, and GitHub Actions**, showcasing a full DevOps lifecycle — from CI/CD to infrastructure automation and monitoring.

---

## 🚀 Features  

- **Frontend (EHR Web UI)** – Built with HTML/CSS/JS, accessible via NodePort service.  
- **Backend (Express.js API)** – Handles patient and appointment data with REST APIs.  
- **Database (MongoDB)** – Stores patient and appointment records persistently.  
- **Containerization (Docker)** – Each component runs in isolated containers.  
- **Orchestration (Kubernetes)** – Deploys and scales the application automatically.  
- **Automation (Ansible)** – Automates environment setup and deployment.  
- **CI/CD (GitHub Actions)** – Builds and pushes Docker images automatically.  
- **Monitoring (Prometheus + Grafana)** – Collects metrics and visualizes application health.

---

## 🧱 Project Architecture  

![Architecture Diagram](docs/architecture.png)  
> *System flow showing how users interact with the frontend, backend, and monitoring stack.*

### 🔹 Key Components
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

## ⚙️ Tech Stack  

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

## 🧩 Project Structure  

