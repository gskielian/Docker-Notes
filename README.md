# Docker-Notes

Notes and Links for getting started with Docker.


## youtube explanations

1. this youtube series discusses Docker's usefulness very clearly:

https://www.youtube.com/watch?v=pGYAg7TMmp0

## hubs

1. like a github for docker images

https://hub.docker.com/

## Basic Commands

These are the commands we'll be using the most:

- docker run <image> #creates a new container each time this is invoked
- docker start <name or id>
- docker stop <name or id>
- docker ps #like linux process status for docker images
- docker rm <name or id> #removes a container

**you'll need to prefix with `sudo` unless you do some additional steps**

Example Workflow for getting started with image called "ubuntu"

- docker login #will ask for your dockerhub login password -- can be set up for alternative hubs

- docker pull ubuntu
- docker run -p 22 -i -t ubuntu /bin/bash #will bring this terminal into the docker image

in a separate window do:
- docker ps # to find the hash of the docker image
- docker commit <current image hash> ur_username/image_name
- docker push ur_username/image_name

...then you have pushed an image to dockerhub

