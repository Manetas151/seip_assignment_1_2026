# Echo API - Cloud Native Deployment

This repository contains the CI/CD pipeline and Kubernetes clusters for auto code deployment

## Before you start
Mke sure you have instaled *Docker **Desktop** and **Minikube** 

## Quickstart Guide

1. **Clone the repository:**
   `git clone https://github.com/Manetas151/seip_assignment_1_2026.git`

2. **Start the local cluster:**
   `minikube start`

3. **Deploy the infrastructure:**
   `kubectl apply -f k8s/`

4. **Access the Application (Port Forwarding):**

   `kubectl port-forward service/echo-api-service 3000:80`

## Endpoints
Once port-forwarding is active, you can interact with the API at:
* **Health Check:** `http://localhost:3000/health`
* **Root (ConfigMap Check):** `http://localhost:3000/`
* **Secure Route (Secret Check):** `http://localhost:3000/secure-config`