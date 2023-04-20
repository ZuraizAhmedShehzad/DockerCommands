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
    # apache image - latest by default
    docker pull httpd 
    
    # apache image - latest specified
    docker pull httpd:latest 
    
    #apache image - 2.9v
    docker pull httpd:2.9 
    ```
- **Start Docker Container**
    ```bash
    # check container id using "docker ps -a"
    docker start container-id 
    ```
- **Stop Docker Container**
    ```bash
    # check container id using "docker ps -a"
    docker stop container-id 
    ```
- **Run Docker Container**
    ```bash
    # run container in terminal
    - docker run redis 
    
    # -d detached is used to run container in background of terminal
    - docker run -d redis 
    
    # -d detached is used to run container in background of terminal
    - docker run -d redis 
    
    # --name is used to specify a name for container
    - docker run -d --name mywebapp redis 
    
    # -p is port, 7000 is host port, 6379 is container port. Host port cant be same for multiple containers
    - docker run -p7000:6379 -d redis 
    ```
    - **docker run** is used to create a new container from an image, while **docker start** is used to start an existing container that has been stopped or paused.
- **Remove Docker Image**
    ```bash
    docker rm image-name 
    
    # -f is used to forcefully delete image if its container is running
    docker rm -f image-name 
    ```
- **Remove Docker Container**
    ```bash
    docker rm container-id 
    
    # -f is used to forcefully delete image if its container is running
    docker rm -f container-id 
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
