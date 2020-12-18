# docker-R-studio

## Description

To allow running customized R Studio in Docker environment

## Procedure
'docker login' - to aunthenticate

'docker build -t redzuan/docker-r-studio .' - to build

'docker images' - listing all images

'docker run --rm -p 8787:8787 -e USER=user -e PASSWORD=password redzuan/docker-r-studio' - Run docker on port 8787 and removed after quit


