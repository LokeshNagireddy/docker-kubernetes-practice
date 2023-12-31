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
* ENTRYPOINT is also used to run the container, but there are some differences.
  - we cant override ENTRYPOINT, but we can override CMD.
  - if you try to override ENTRYPOINT, it will go and append to the actual command given in Dockerfile.
  - Therefore you can give an extension command which is not reccommended in best practices.
  - If you use both CMD and ENTRYPOINT, dont give any command from terminal. CMD will act as Arguement provided to ENTRYPOINT.
  - In other words, CMD will supply default arguments to ENTRYPOINT. you can always override CMD arguments from terminal.
* USER
* WORKDIR - it is used to set the path to the image.
  - docker control will go to default directory after running every command (like RUN). To overcome this behaviour, we can set the working path (or) directory using WORKDIR instruction.
* ARG - this instruction is used to provide arguments to container at the time of image creation. 
  - Its the only instruction that can be used before FROM in a Dockerfile.
  - ARG declared before FROM cannot be used after FROM. you have to declare the argument again after FROM to get the arguments given externally.
  - Use ENV and ARG for best results.
* ONBUILD - This is instruction is used to set some hard guidelines on the image.
* STOPSIGNAL - This instruction is used to define how to exist the container.
   - By default, docker requests for exit and wait for some time. if its not exiting it can force kil.
   - when your container receives stop signal, your application can perform, closing files, databases etc to avoid data loss etc..
   - Developers will take care of how to use STOPSIGNAL to avoid abrupt stopping of container.
* VOLUME - docker volumes are ephemeral, when you remove a container, by default it will delete all data.
   - docker volumes are stored in /var/lib/docker/volumes.
   - when you create a volume and mount it to container, the data will not be deleted when container was removed.
   - We can create a directory and attach it as a volume instead of creating a docker volume, it is called anonymous volumes. Docker dont manage these volumes/directories.