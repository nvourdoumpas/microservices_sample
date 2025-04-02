# Microservices Sample with .net core

## Table of Contents

- [About](#about)
- [Prerequisites](#prerequisites)
- [Deployment](#deployment)

## About <a name = "about"></a>

This project created for education proposes about <i>Microservices, Containers, Docker, Docker Hub, Kubernetes, API Gateway, Message BUS & RABBITMQ</i> technologies using .NET Core. <br />
Original course: [.NET Microservices – Full Course](https://www.youtube.com/watch?v=DgVjEo3OGBI) <br />
Author: [Les Jackson](https://lesjackson.net/) <br />

## Prerequisites <a name = "prerequisites"></a>

- VS Code (C# Dev Kit, Docker, Kuberetes extensions)
- Docker for Desktop (With enable kubernetes)
- .net core 5 SDK
- Postman

## Deployment <a name = "deployment"></a>

- [Kubernetes](#kubernetes)
- [Docker](#docker)

### Kubernetes Commands <a name = "kubernetes"></a>

- Apply kubernetes deployment configuration

```
kubectl apply -f K8S/platforms-depl.yaml
```

- Show status of kubernetes deployments

```
kubectl get deployments
```

- Restart kubernetes deployments to take changes of image

```
kubectl rollout restart deployment platforms-depl
```

- Delete kubernetes deployment

```
kubectl delete deployment platforms-depl
```

- Show status of kubernetes pods

```
kubectl get pods
```

- Show status of kubernetes services (e.g NodePort)

```
kubectl get services
```

- Apply depleoyment of ingress nginx (for API Gateway)

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.12.1/deploy/static/provider/cloud/deploy.yaml
```

- Get all namespaces and get pods for specific namespace (e.g. ingress nginx)

```
kubectl get namespaces
```

```
kubectl get pods --namespace=ingress-nginx
```

- Show storage status

```
kubectl get storageclass
```

- Show Persistent Volume Claim status

```
kubectl get pvc
```

### Docker Commands <a name = "docker"></a>

- Build image local

```
docker build -t nvour/platformservice ./PlatformService
```

- Create container from image

```
docker run -d --name platformservice -p 8080:80 nvour/platformservice
```

- Start-Stop-Remove container (by name or id)

```
docker stop platformservice
```

```
docker rm platformservice
```

```
docker start platformservice
```

- Push image to dockerhub

```
docker push nvour/platformservice
```
