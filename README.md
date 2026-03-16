# DevOps Kubernetes Project

Este projeto demonstra o deploy de uma aplicação containerizada utilizando Kubernetes em uma instância AWS EC2.

O objetivo foi praticar conceitos importantes de DevOps como containerização, orquestração de containers e exposição de serviços dentro de um cluster Kubernetes.

---

## Arquitetura

User (Browser)
↓
Internet
↓
AWS EC2 Instance
↓
K3s Kubernetes Cluster
↓
Nginx Deployment (Pods)
↓
Kubernetes Service (NodePort)
↓
Aplicação acessível no navegador

---

## Tecnologias utilizadas

- AWS EC2
- Kubernetes (K3s)
- Docker
- Nginx
- Linux
- Git
- GitHub

---

## Deploy da aplicação

Criar deployment:

kubectl create deployment nginx-deployment --image=nginx

Verificar pods:

kubectl get pods

Expor aplicação:

kubectl expose deployment nginx-deployment --type=NodePort --port=80

Verificar serviço:

kubectl get svc

---

## Acesso à aplicação

Após expor o serviço, a aplicação pode ser acessada pelo navegador utilizando o IP público da instância EC2 e a porta NodePort.

Exemplo:

http://100.26.42.81:31351

Isso exibirá a página padrão do Nginx rodando dentro do Kubernetes.

---

## DevOps Pipeline Architecture

```mermaid
flowchart TD
    A[Developer] --> B[GitHub Repository]
    B --> C[GitHub Actions CI/CD]
    C --> D[Build Docker Image]
    D --> E[Push Docker Image to DockerHub]
    E --> F[Kubernetes Cluster]
    F --> G[Deployment]
    G --> H[Pods]
    H --> I[Service NodePort]
    I --> J[Application Access]

    F --> K[Prometheus Monitoring]
    K --> L[Grafana Dashboards]
```
---

## Objetivo do projeto

Este projeto foi criado para praticar:

- Deploy de aplicações em Kubernetes
- Estrutura de um cluster Kubernetes
- Exposição de serviços com NodePort
- Integração entre Docker, Kubernetes e AWS

---
## Autora

Rayane Santana
