<<<<<<< HEAD
# Project 1: Local Kubernetes Cluster Setup with Minikube

## Overview
Set up a local Kubernetes cluster using Minikube and deployed an Nginx web application.

## Tools Used
- Minikube v1.38.1
- kubectl v1.36.1
- Docker Desktop
- Ubuntu (WSL2)

## What I Did
- Started a local K8s cluster using Minikube
- Created and deployed a Pod using YAML manifest
- Created a Deployment with 2 replicas
- Exposed the app as a NodePort Service
- Accessed live Nginx app in browser

## Commands Used
```bash
minikube start --driver=docker
kubectl apply -f pod.yaml
kubectl apply -f deployment.yaml
kubectl expose deployment nginx-deployment --type=NodePort --port=80
minikube service nginx-deployment --url
```
=======
# Project B: Kubernetes ConfigMaps & Secrets

## What I Did
- Created a ConfigMap to store app configuration
- Created a Secret to store sensitive data (passwords, API keys)
- Deployed a Pod that reads values from both ConfigMap and Secret
- Verified env variables inside the pod using kubectl exec

## What I Learned
- ConfigMaps store non-sensitive config (env name, ports, URLs)
- Secrets store sensitive data in base64 encoded format
- Pods can inject these values as environment variables

## Commands Used
kubectl apply -f configmap.yaml
kubectl apply -f secret.yaml
kubectl apply -f pod-with-config.yaml
kubectl exec myapp-pod -- env | grep -E "APP_ENV|APP_NAME|DB_PASSWORD|API_KEY"
>>>>>>> c9f59d8 (Add Project B - ConfigMaps and Secrets)
