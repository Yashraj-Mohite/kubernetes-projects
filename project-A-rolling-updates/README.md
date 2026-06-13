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
