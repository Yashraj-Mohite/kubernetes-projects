# Project C: Kubernetes Resource Limits & Health Checks

## What I Did
- Set CPU and memory requests/limits on containers
- Added liveness probe to auto-restart unhealthy pods
- Added readiness probe to control traffic flow to pods
- Verified configuration using kubectl describe pod

## What I Learned
- Requests = guaranteed minimum resources for a container
- Limits = maximum resources a container can use
- Liveness probe = restarts the pod if app becomes unresponsive
- Readiness probe = stops traffic to pod until it's ready

## Commands Used
kubectl apply -f deployment.yaml
kubectl get pods
kubectl describe pod <pod-name>
