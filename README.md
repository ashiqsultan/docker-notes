# docker-notes

Youtube: [Full Video Link](https://www.youtube.com/watch?v=fqMOX6JJhGo)
## Basics
- A Docker is like any other service running on an OS
- A Docker runs other process like Redis or Nginx, we call each process run by the docker as **Container**
- Docker is not ment to run OS as a process
- Its for running an instance of web application, a server or just a computation
- Terminology: A Docker Host or host machine means the machine running the docker deamon

## Difference between Docker and traditional VM
- An OS runs inside VM which runs services like Redis or MongoDB
- A Docker runs services like MongoDB or Redis without the need of OS

## A container is alive only as long as the process inside is alive
- Once the task or computaion stops or completes or crashes the container exists
- i.e the container is alive as long as the process inside is alive
- That's why if you run an Ubuntu image as a container it exits immediately, because an OS doesn't run any process by default
- If you want you could execute a command for the process (container) which is going to be started by the docker run
```
docker run ubuntu sleep 100
docker run imagename command-to-be-executed-in-the-starting-container
```
In the above example the container executes the Sleep for 100 seconds and the container exits or stops after the command has finished executing

## Creating new containers
Runs the process if the image of Redis is present else downloads it from the public repository
- docker run redis
Pull only the Image without running
- docker pull nginx

## Basic commands
Outputs a list of docker containers
- docker ps
- docker ps -a
- docker container -ls

List the available images in the host
- docker images
Remove An image form the host
Caution: Make sure no containers are attached to the image before removing an image
- docker -rmi imagename

## Image Tag
Image tag is the version of image you want to download from the docker hub. By default it downloads the latest tag

## Port mapping
`docker run -p 80:5000 imageName`
The above command is map a container running on port 5000 when port 80 is requested from the Host machine

## Inspect
Gives details about the container
docker inspect containerName

## Environment Variables
` docker run -e NODE_ENV=production imageNAme`
