# NestJS Kubernetes Application

This guide will walk you through building the Docker image for your NestJS application and deploying it to a Kubernetes cluster.

## Prerequisites

- [Kubernetes](https://kubernetes.io/docs/tasks/tools/) (Minikube or any K8s cluster)
- [kubectl](https://kubernetes.io/docs/reference/kubectl/) installed

## Steps

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Build Docker Image

```bash
docker build -t your-docker-image:latest .
```

### 3. Run Kubernetes Deployment

```bash
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
```

### 4. Verify the Deployment

```bash
kubectl get deployments
```

### 5. Verify the Service

```bash
kubectl get services
```

### 6. Cleaning Up

```bash
kubectl delete -f kubernetes/deployment.yaml
kubectl delete -f kubernetes/service.yaml
```
