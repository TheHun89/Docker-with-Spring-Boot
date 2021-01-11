# Docker with Spring Boot

* [Spring Boot MongoDB and Multi-Container Apps with Docker Compose](https://nirajsonawane.github.io/2019/12/16/Spring-Boot-Mongodb-Docker-Compose/)
* [Medium - Spring Boot and MongoDB running on Docker containers](https://medium.com/@volmar.oliveira.jr/a-restapi-using-spring-boot-mongodb-running-on-docker-containers-5e530b48f45e) (Using the docker maven plugin we are able to build a new image and publish if it is the case during Maven pipeline, on this example we will build a new image on every mvn package.)
* [Medium - Benefits of using Docker](https://medium.com/uptime-99/the-benefits-of-using-docker-for-development-and-operations-2c5256ad89bc)

* [Youtube - Create Docker Image with Spring Boot](https://www.youtube.com/watch?v=FlSup_eelYE)
* [Publish Docker Images on Private Nexus Repository Using Jib Maven Plugin](https://dzone.com/articles/how-to-publish-docker-images-on-private-nexus-repo-1)


* if updates are made to SB app then you just need to rerun - mvn package
* docker-compose up/down
* docker images
* docker volume ls
* docker system prune -a (To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:)
* docker container ls -all
* docker ps (show only running containers; use -a to show all containers)

* [Volumes](https://docs.docker.com/engine/reference/commandline/volume_ls/)
