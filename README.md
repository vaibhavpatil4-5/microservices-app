# 🚀 Java Microservices Deployment on AWS EKS

This project demonstrates a complete **cloud-native microservices architecture** deployed on **Amazon EKS (Elastic Kubernetes Service)** using **Docker, Kubernetes, GitHub Actions CI/CD, and AWS Load Balancer (ALB Ingress)**.

It follows modern DevOps practices for containerized application deployment and automated delivery.

---

## 🧩 Architecture Overview

Internet → AWS Application Load Balancer → Kubernetes Ingress → Service → Pods

The system consists of multiple Java-based microservices packaged as Docker containers and deployed on Kubernetes.

---

## 🛠 Tech Stack

- Java (Spring Boot)
- Docker (Containerization)
- Kubernetes (EKS)
- AWS Load Balancer Controller (ALB Ingress)
- GitHub Actions (CI/CD)
- kubectl (Cluster management)
- Maven (Build tool)

---

## 📦 Microservices

- Catalog Service
- Customer Service
- Order Service

Each microservice runs in its own Kubernetes Deployment and communicates through internal services.

---

## ⚙️ CI/CD Pipeline

Automated using GitHub Actions.

Pipeline flow:

1. Push code to `main` branch
2. Build microservices using Maven
3. Deploy Kubernetes manifests
4. Update workloads in EKS cluster
5. Load Balancer routes external traffic

Deployment happens only if all builds succeed.

---

## 🌐 Load Balancer & Ingress

- AWS Application Load Balancer (ALB)
- Internet-facing traffic routing
- Path-based routing supported
- External access to microservices

Example endpoint:

