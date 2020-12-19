# docker-R-studio

## Description

To running customized R Studio in Docker environment

## Procedure

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

Press ctrl + c - Kill container