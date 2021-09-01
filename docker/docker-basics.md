## Docker Basics

> Platform as a service product that uses OS level **virtualization** to deliver software in **containers**

### Why use Docker

1. Allow for replication of applications on different platforms.
1. Allow for setup of isolated environments on the same server.
1. Allow for scaling services as and when needed.


### Definitions
1. Images
    - Immutable layers created to execute a function.
    - These layers are defined within an instructional file - **Dockerfile**

2. Containers
    - isolated environments in a host machine that can interact with each other and the host machine itself.
    - Are built based on the docker image definitions.

### Docker Commands cheatsheet.

1. `docker container run <image_name>`
    - How does it work?
        1. the docker client contacts the Docker daemon, via a rest API.
        2. the daemon finds and pulls the listed image from the docker hub,
        3. then creates a new container and executes the image commands.
    - Note that, at step 2,the daemon first cheks if the image is available locally before pulling it again.

1. `docker container ls`
    - Output a list of containers on the host machine.

1. `docker container rm <container_id/container_name>`
    - Remove container from host machine.

1. `docker system prune`
    - cleanup host machine of dangling /unused containers or images.


