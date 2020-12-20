# docker-R-studio

## Description

To running customized R Studio in Docker environment

## Procedure for basic operations

### Docker login
docker login


### Docker built

docker build -t redzuan/docker-r-studio .


### Listing all Docker images
docker images



### Run docker on port 8787 and removed after quit

docker run --rm -p 8787:8787 -e USER=user -e PASSWORD=password redzuan/docker-r-studio



### List all directories in container

docker run --rm -p 8787:8787 -e USER=user -e PASSWORD=password redzuan/docker-r-studio ls -a


### Run docker and map to Window directory. This is however not stored in the image

docker run --rm -p 8787:8787 -e USER=user -e PASSWORD=password -v c:/Temp_for_docker/Docker_R_Studio:/home/user redzuan/docker-r-studio


### Push to Docker Hub
docker push redzuan/docker-r-studio


### Save image locally

docker save redzuan/docker-r-studio > docker-r-studio.tar


### Load Docker image

docker load --input docker-r-studio.tar


### Remove container

docker rmi bf756fb1ae65

pass image ID to Docker rmi command

### Check running Docker
docker container ls
docker container ps
docker ps


### Enter into running container
docker exec -it 7217551d7328 ls
or enter bash docker exec -it 7217551d7328 bash

Command means to execute in interative


### Resave image after updated

While updated container is still running,

docker commit -m "Added gapminder library" 2d9a63213960 redzuan/docker-r-studio


### Push to Docker Hub
docker push redzuan/docker-r-studio

### Deleting un-used container

docker system prune


### Kill Docker image
Press ctrl + c - Kill container