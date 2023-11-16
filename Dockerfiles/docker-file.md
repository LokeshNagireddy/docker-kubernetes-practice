### Notes about Docker file

* Docker file is a declarative way of creating our own images
* Docker will give us some syntax to create our own images.
* file name should be "Dockerfile"

## Instructions
* FROM : first instruction should be a base OS with the required version.

### Building an image from a docker file.
# Command:
```
docker build -t [docker-hub URL]/[username]/[image-name]:version .
```

### How to push an image to dockerhub

1. login to docker using  - "docker login", provide user id and password.
2. then run the below command with the required image with its version.
```
docker push [docker-hub URL]/[username]/[image-name]:version
```

* RUN : RUN instruction is used to install software, packages and other tasks. It runs at the time of image building.
* CMD : CMD is the instruction that runs the container.

### Difference between RUN and CMD
* RUN Command is used at the time of image creation
* CMD is used to run the container (at the time of container creation)

* In a Dockerfile, only one CMD should be there, if there are more than one CMD commands, the last one will get processed.

* LABEL is used to tag the images with some Label name, so that it is helpful to filter in the pile of images.
* EXPOSE instruction is useful to tell the users about the ports and protocols image/container is opening. It will not have any functionality it used only to tell the information.
* ENV is the instruction used to provide environment variables to the containers. you can override the ENV variables at runtime.
* COPY instruction is used to copy your files from local to container.
* ADD is similar to COPY, it can copy files from local to container. Also it has two additional capabilities.
  - ADD can download a file from internet to container.
  - ADD can untar/unzip directly into the container.
