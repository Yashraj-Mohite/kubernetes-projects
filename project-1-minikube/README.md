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
