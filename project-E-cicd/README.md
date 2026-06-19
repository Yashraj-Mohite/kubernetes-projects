# Project E: CI/CD Pipeline with GitHub Actions

## What I Did
- Built a simple Dockerized static web app (nginx + custom HTML)
- Created a GitHub Actions workflow (.github/workflows/docker-build.yml) that automatically builds and pushes the Docker image to Docker Hub on every push to main
- Configured Docker Hub authentication securely using GitHub Repository Secrets
- Verified the pipeline by checking automated builds in the Actions tab and confirming the image updates on Docker Hub

## What I Learned
- GitHub Actions workflow files must live in .github/workflows/ at the repository root
- Secrets (API tokens, credentials) should never be hardcoded — GitHub Secrets keep them encrypted and injected securely at runtime
- Docker build context must point to the folder containing the Dockerfile, especially in monorepo-style setups
- How to debug failed CI/CD runs using the Actions tab logs

## Docker Hub
docker pull yashrajmohite9/cicd-demo

## Workflow File
.github/workflows/docker-build.yml (Docker Hub credentials stored as GitHub Secrets: DOCKERHUB_USERNAME, DOCKERHUB_TOKEN)
