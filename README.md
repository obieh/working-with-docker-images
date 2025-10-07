# Working with Docker images.

## This project will show how to work with docker images. Create and run docker file to build image. Run containers from the built image.

### Docker Images: Docker images are read-only templates that contain instructions for creating a container. A Docker image is a snapshot or blueprint of the libraries and dependencies required inside a container for an application to run.

### [Docker Hub](https://hub.docker.com/) is a cloud registry that hostd a vast collection of images. You can pull from docker to your local machine as well as push from your local machine to docker cloud registry.

### Search Images on Docker Hub
* To search image from docker hub, run, example ubuntu `docker search ubuntu`

![](./img/Pasted%20image.png)

### Pulling Images from Docker Hub
* To pull images from docker hub run `docker pull`

![](./img/Pasted%20image%20(3).png)

* Run `docker images` to very image pull.

![](./img/Pasted%20image%20(2).png)

### Dockerfile: A text file with instructions to build a custom image. Not shown in architecture diagrams but essential. 
1. Use your text editor to create a file named 'Dockerfile'

```Dockerfile
# Use the official NGINX base image
FROM nginx:latest

# Set the working directory in the container
WORKDIR  /usr/share/nginx/html/

# Copy the local HTML file to the NGINX default public directory
COPY index.html /usr/share/nginx/html/

# Expose port 80 to allow external access
EXPOSE 80

# No need for CMD as NGINX image comes with a default CMD to start the server.
```

![](./img/Pasted%20image%20(4).png)

2. Run this command to create html file, `echo '<h1> Welcome to darey.io</h1>' `

![](./img/Pasted%20image%20(5).png)

