# ums-dk-s02-1244330

Sezione 2: Docker Images &amp; Containers: The Core Building Blocks - Schwarzmuller

# Run node-app

### 1. Create image

docker build .

### 2. Run container for the image

docker run -p 80:3000 -d <image-id>

### 3. Re-create containers and assign name

docker stop <container-id>
docker run -p 80:3000 -d --name <container-name-id> <image-id>

### 4. Clean up (remove) all stopped (and running) containers, clean up all created images.

docker stop <container-name-id>
docker ps -a
docker rm <container-id>
docker images
docker rmi <image-id>

### 5. Re-build the images - this time with names and tags assigned to them.

docker build -t hello-world-image:latest .

### 6. Run new containers based on the re-built images and use removed automatically option when stopped.

docker run -p 80:3000 -d --rm --name <container-name-id> <image-id>

# Run python-app

### 1. Create image

docker build .

### 2. Run container for the image

docker run -it <image-id>

### 3. Re-create containers and assign name

docker container ls -a
docker rm <container-id>
docker run -it --name <container-name-id> <image-id>

### 4. Clean up (remove) all stopped (and running) containers, clean up all created images.

docker stop <container-name-id>
docker ps -a
docker rm <container-id>
docker images
docker rmi <image-id>

### 5. Re-build the images - this time with names and tags assigned to them.

docker build -t bmi-python-image:latest .

### 6. Run new containers based on the re-built images and use removed automatically option when stopped.

docker run -it --rm --name <container-name-id> <image-id>
