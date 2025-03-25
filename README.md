# ----- DOCKER COMMANDS -----

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
