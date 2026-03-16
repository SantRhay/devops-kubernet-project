# DevOps Kubernetes Project

This project demonstrates a DevOps architecture using Kubernetes running on AWS EC2.

---

# Architecture

User (Browser)
      │
      ▼
Internet
      │
      ▼
AWS EC2 Instance
      │
      ▼
K3s Kubernetes Cluster
      │
      ▼
Nginx Deployment (Pods)
      │
      ▼
Kubernetes Service (NodePort)
      │
      ▼
Application accessible in browser

---

# Technologies Used

- AWS EC2
- Kubernetes (K3s)
- Docker
- Nginx
- Git
- GitHub

---

# Kubernetes Deployment

Deployment file:


k8s/deployment.yaml


Service file:


k8s/service.yaml


---

# Access Application


http://100.26.42.81:30007


This will display the Nginx Welcome Page running inside Kubernetes.
