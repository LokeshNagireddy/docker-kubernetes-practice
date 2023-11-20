### Some Common and Important Docker Commands

1. docker images            - will show all images available in the server.
2. docker pull <image-name> - will pull the image from the server. if version was provided, it will pull the image of that version, otherwise it will pull the latest version.
3. docker create <image-id> - will create the container from the given image.
4. docker ps                - will show all running containers.
5. docker ps -a             - will show all containers irrespective of state.
6. docker start <container-id>  - will start the container and it will be running state.
7. docker stop <container-id>   - will stop the container
8. docker rm <container-id>     - will remove the container (stopped container)
9. docker rm -f <container-id>  - To remove a running container (-f denotes force stop and remove)
10. docker rmi <image-id>       - will remove the image
11. docker rm -f 'docker ps -a -q'  -- To remove all containers at once.
12. docker run <image-name>     - will pull the image, it will create the container and start the container. its equal to three docker commands (pull + create + start). It attaches to the screen.
13. docker run -d <image-name>  - To create and run container in dettached mode(back ground).
14. docker run -d -p <host-port:container-port> <image-name> - for port assignment to the container
15. docker run -d -p 80:80 --name <any meaningful name> <container-id> <image-name> - for assigning a name to the container
16. docker exec -it <container-id> bash - To login into the container and connect to bash terminal
17. ctrl + D    - To come out of the container
18. docker build -t [docker-hub URL]/[username]/[image-name]:version .  --> to build your own image from docker hub.
19. docker ps -a -q - provides all container ids.
20. docker inspect <container-id>   - To find all basic and networking information of that container.
21. docker logs <container-id>      - To see the logs of the container.

