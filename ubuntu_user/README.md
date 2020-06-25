# dockerfiles-ubuntu-user-adderable
Ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build thegabrielus-kim container, and to run.
```
	docker build --rm -t gabrielus-kim/ubuntu .
	docker run -it --name u1 -e USER=nowage -e PASSWD=nowage gabrielus-kim/ubuntu
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        gabrielus-kim/ubuntu      "/bin/bash"         7 seconds ago       Up 6 seconds                            u1
```

To test, ("gabrielus-kim" is username. )
```
	su - gabrielus-kim
```
To Rollback
```
    docker rm u1 -f
    docker rmi gabrielus-kim/ubuntu
```
