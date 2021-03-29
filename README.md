# Docker

hub.docker.com is a registry containts multiple respository which holds images of the application.

the images nothing but a set of bytes

once it start run then it can be called as container

image is static version
and container is running version

for an image we can run multiple container.

# Docker Architecture

Once we install docker desktop, it install Docker client and Docker Daemon. Once we execute any command the command will reach to Docker Daemon which is responsible to maintain containers, local images and docker registry.


# Deployments using VM

it use Hypervisor deploy application. And VM has two OS, HostOS and GuestOS which makes the system heavy.


# Docker commands

1. docker image history tagname. -> it will provide history changes happened on the specific tag
2. docker image inspect tagname -> it provide information about when it was created, configuration, entrypoint, folder structure, layer details, etc.
3. docker image remove imageId-> remove from image from local not from repository.
4. docker pause imageId -> it will pause the container/application
5. docker unpause imageId -> it will resume the container/application
6. docker prune -> it will remove all paused docker container from local
7. docker ps -> provides actively running container details
8. docker ps -a -> it provides all the images available locally
9. docker logs -f imageId -> using this we can tail the application log
10. docker stop imageId -> it gracefully stopp the container. Once the command executed the signal send to the container called SIGTERM, means it take 10 sec to stop container gracefully
11. docker kill imageId -> it stop a container forcefully. a signal SIGKILL will be send down to the container to terminate the process immediately.
12. docker events -> it will list all the events happening
13. docker top imageId -> used to display top process running in a container
14. docker stats -> all the stats regarding container which are running
15. docker system df -> it will list all different things managed by docker daemon
16. docker run -m 512m --cpu-quota 50000 -> it start a specific container with max usage of 521 MB size and give cpu limits to use.
