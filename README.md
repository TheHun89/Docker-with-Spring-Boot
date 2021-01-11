# Docker with Spring Boot

* [Spring Boot MongoDB and Multi-Container Apps with Docker Compose](https://nirajsonawane.github.io/2019/12/16/Spring-Boot-Mongodb-Docker-Compose/)
* [Medium - Spring Boot and MongoDB running on Docker containers](https://medium.com/@volmar.oliveira.jr/a-restapi-using-spring-boot-mongodb-running-on-docker-containers-5e530b48f45e) (Using the docker maven plugin we are able to build a new image and publish if it is the case during Maven pipeline, on this example we will build a new image on every mvn package.)
* [Medium - Benefits of using Docker](https://medium.com/uptime-99/the-benefits-of-using-docker-for-development-and-operations-2c5256ad89bc)

* [Youtube - Create Docker Image with Spring Boot](https://www.youtube.com/watch?v=FlSup_eelYE)
* [Publish Docker Images on Private Nexus Repository Using Jib Maven Plugin](https://dzone.com/articles/how-to-publish-docker-images-on-private-nexus-repo-1)


* Using Docker Desktop

* DockerHub Registry can contain multiple repositories where you can load images (and their versions/tags) for public use to pull down
* image is a static template/set of bites that contains everything your app needs to run - all the classes, libraries and dependencies
* images are ran in containers and you can have multiple containers running at once

Manually:

* docker run -p 5000:5000 in28min/todo-rest-api-h2:1.0.0.RELEASE  (this is downloading an image - and its specific tag - from DockerHub; if you stop the image and then run it again you will notice it doesn't download the image again; however, if you change the version/tag of the image then it will know to download a new one)
* -p {hostport:containerport} (you are saying you want to map a containerport to a specific hostport)

* docker run -p 5001:5000 -d in28min/todo-rest-api-h2:1.0.0.RELEASE  (-d makes it run in detached mode in the background; notice we are also using port 5001 - we are running multiple instances of the same container!; NOTE - also run the first instance with -d)

* docker logs -f <first few characters of container instance> (this lets us tail the logs for one of the container instances)
  
* docker pull mysql (automatically pulls down latest image for mysql; does not run it)
  
* these docker commands are ran in the Docker Client and are sent to the Docker Daemon/Engine

![Docker Architecture](https://docs.docker.com/engine/images/architecture.svg)

* if updates are made to SB app then you just need to rerun - mvn package
* docker --version
* docker-compose up/down
* Ctrl + C to stop the running container
* docker images
* docker volume ls
* docker system prune -a (To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:)
* docker container ls -all (show all containers with -all, exclude it to only show those running)
* docker ps (show only running containers; use -a to show all containers)

* [Volumes](https://docs.docker.com/engine/reference/commandline/volume_ls/)
