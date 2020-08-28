# docker-notes

Youtuube: [Full Video Link](https://www.youtube.com/watch?v=fqMOX6JJhGo)
## Basics
Docker runs on top of an OS. In other words a OS runs a single docker service
Difference between docker and traditional VM is that
- An OS runs inside VM which runs services like Redis or MongoDB
- A Docker runs services like MongoDB or Redis without the need of OS

So as soon as the process is stopped the docker is also stopped

## Creating new containers
- docker run nginx
- docker run redis

Runs the process if the image of Redis is present else downloads it from the public repository

## Basic commands
- docker ps
Outputs a list of docker containers
- docker container -ls
Same as above
- docker images
List the available images
