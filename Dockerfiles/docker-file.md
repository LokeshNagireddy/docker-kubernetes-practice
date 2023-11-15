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