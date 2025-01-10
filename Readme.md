## Docker
Docker is an open-source platform designed to automate the development, shipping, and running of applications using containers. 
Containers are lightweight, portable, and isolated environments that allow you to package an application with its dependencies, ensuring consistency across different environments.

## Docker Architecture

![image](https://github.com/user-attachments/assets/a97d28f1-2708-495f-871d-365b8c1c2b3a)


## Components of Docker 
**1.Containers** 
   
   - Containers are isolated environments where applications run. They package the application along with its libraries, dependencies, and configuration files, ensuring that it runs consistently regardless of the host environment.
  
   - Containers share the same operating system kernel, making them lightweight and efficient compared to virtual machines.

**2.Docker Images**
 
   - A Docker image is a snapshot of an application and its dependencies. It is a read-only template that defines the environment in which the container runs.
   
   - Docker images are built using a Dockerfile, which contains a set of instructions on how to assemble the image.

**3.Docker Engine**

   - The Docker Engine is the runtime that runs and manages containers. It is available for multiple platforms like Linux, macOS, and Windows.
   
   - It is responsible for building images, running containers, and managing resources.

**4.Dockerfile**

   - A Dockerfile is a script containing a series of instructions that define how a Docker image should be built. It typically includes base images, dependencies, and 
     commands to run inside the container.

**5.Docker Hub**

  - Docker Hub is a cloud-based registry service that allows users to store, share, and download Docker images.
  
  - It contains many publicly available images for popular applications and services.

**6.Docker Compose**

  - Docker Compose is a tool for defining and running multi-container Docker applications. It uses a docker-compose.yml file to configure the application's services, 
    networks, and volumes.

**7.Docker Registry**

  - A registry is a place where Docker images are stored. Docker Hub is the default public registry, but you can also set up private registries for internal use.

## Basic Commands for Docker

**Build an Image**
````
docker build -t my-image .
````
**Run a Container**
````
docker run -d --name my-container my-image
````
**List running Containers**
````
docker ps
````
**List all Container**
````
docker ps -a
````
**Stop Container**
````
docker stop my-container
````
**Remove Container**
````
docker rm my-container
````
**Pull Image**
````
docker pull ubuntu  #Image Name
````
**Push an image to Docker Hub**
````
docker push my-image
````
**List last container**
````
docker ps -l
````
**Removing Images**
````
docker rmi <image-name|id>
````
**Delete all Images**
````
docker rmi $(docker images -q)
````
**Kill running Container**
````
if [ "$(docker ps -q)" ]; then docker kill $(docker ps -q); else echo "No running containers."; fi
````
**Get IP Address**
````
docker inspect $(dl) | grep -wm1 IPAddress | cut -d '"' -f 4
````
**List of Docker with Format**
````
docker ps --format $FORMAT
````
**Kill a Container**
````
docker kill <container-name>
````

## Install Docker 

````
sudo apt install docker.io
sudo systemctl start docker # To start Docker
sudo usermod -aG docker ubuntu # This will add ubuntu to docker group 
newgrp docker # refresh
docker --version
````

**To Check Docker Status**
````
docker info
````
