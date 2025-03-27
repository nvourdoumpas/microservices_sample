# ----- KUBERNETES COMMANDS -----

# Apply kubernetes deployment configuration

kubectl apply -f K8S/platforms-depl.yaml

# Show status of kubernetes deployments

kubectl get deployments

# Delete kubernetes deployment

kubectl delete deployment platforms-depl

# Show status of kubernetes pods

kubectl get pods

# Show status of kubernetes services (e.g NodePort)

kubectl get services

# ----- DOCKER COMMANDS -----

cd PlatformService

# Build image local

docker build -t nvour/platformservice .

# Create container from image

docker run -d --name platformservice -p 8080:80 nvour/platformservice

# Start-Stop-Remove container (by name or id)

docker stop platformservice
docker rm platformservice
docker start platformservice

# Push image to dockerhub

docker push nvour/platformservice
