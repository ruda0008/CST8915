
# Docker Reflection Questions

## 1. What are the main differences between a Docker image and a Docker container?

- Docker image is a static read only file that allows to defines what's needed to run an application including codem libraries, dependencies, configurations, environments and more. While on the other hand docker container is a running instance of docker image. A live isolated environment where the application actually executes.

## 2. How Docker’s layered architecture improves efficiency

- Docker images are built in layers, each layer represents different change like installing dependencies, copying file and more. The layers are cached thus docker only rebuils changes and uses unchanged data from cache insted of building from scratch. The layered structure saves disk space, faster build, and quicker distribution.

## 3. Why each container gets its own writable layer

- Each container gets their own writable layer on top of read only image layer so that it can store additional data like runtime data, config changes, temporary files without affecting the origianl image. This helps to isolate the containers from one another. Any changes made inside the container doesn't impact other or the orginal image.


## 4. Benefits of using Docker Compose over running containers individually

- By just using a single YAML file, Docker Compose allows users to define and administer multi-container applications. Streamlines setups, networking, and dependencies by automating the process. It manually launches each container with commands making it easy and simple to start, pause, or scale the application stack with a single command, guarantees consistency across environments, and configuration and more.

# Youtube link 
 - https://youtu.be/DNpo5OUl-S0 