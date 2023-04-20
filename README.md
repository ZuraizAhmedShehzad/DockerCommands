# Docker Commands

- **Start Hello World Container**
    ```bash
    docker run hello-world
    ```
- **List of Containers:**
    ```bash
    docker ps
    ```
    ```bash
    docker ps -a
    ```
    - docker: This is the command-line interface (CLI) for interacting with the Docker engine.
    - ps: This is the Docker command for listing containers.
    - a: This is an optional flag that tells Docker to show all containers, including those that are not currently running.
- ******************************List of Images:******************************
    ```bash
    docker images
    ```
- **Search Images From Docker Hub:**
    ```bash
    docker search  apache 
    ```
- **Pull Docker Image**
    ```bash
    docker pull httpd (apache image - latest by default)
    
    docker pull httpd:latest (apache image - latest specified)
    
    docker pull httpd:2.9 (apache image - 2.9v)
    ```
- **Start Docker Container**
    ```bash
    docker start container-id (check container id using ‘docker ps -a’)
    ```
- **Stop Docker Container**
    ```bash
    docker stop container-id (check container id using ‘docker ps -a’)
    ```
- **Run Docker Container**
    ```bash
    - docker run redis (run container in terminal)
    - docker run -d redis (-d detached is used to run container in background of terminal)
    - docker run -d redis (-d detached is used to run container in background of terminal)
    - docker run -d --name mywebapp redis (--name is used to specify a name for container)
    - docker run -p7000:6379 -d redis (-p is port, 7000 is host port, 6379 is container port. Host port cant be same for multiple containers)
    ```
    - **docker run** is used to create a new container from an image, while **docker start** is used to start an existing container that has been stopped or paused.
- **Remove Docker Image**
    ```bash
    docker rm image-name 
    
    docker rm -f image-name (-f is used to forcefully delete image if its container is running)
    ```
- **Remove Docker Container**
    ```bash
    docker rm container-id 
    
    docker rm -f container-id (-f is used to forcefully delete image if its container is running)
    ```
- **Check Docker Logs**
    ```bash
    - docker logs container-id
    - docker logs container-name
    ```
- **Connect with Container**
    ```bash
    - docker exec -it container-id/container-name /bin/bash
    ```
    - In the docker exec command, the -it option is used to create an interactive terminal session inside a running container.
    - Bash is a powerful command-line interface that allows you to interact with the operating system and execute various commands and scripts. When you start a new instance of Bash within a container, you can use it to navigate the container's file system, install software, edit files, and perform other system-level tasks.
    - use “exit” to get out of container.
- **Command Manual:**
    
    write man before any command to check possible flags that can be used with it.
    
    eg. man docker-images
