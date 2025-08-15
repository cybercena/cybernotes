### Docker Run Command
This command is used to run a container from an image. The docker run command is a combination of the docker create and docker start commands. it creates a new container the images specified and starts that container. if the docker images is not present, then the docker run pulls that.

```
docker run <imagekoname>
To give name of container
docker run --name <containername> <imagekoname>
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/docker-run.png?raw=true)

![](https://github.com/cybercena/Static-assets/blob/main/Docker/docker-name.png?raw=true)

### Docker Pull
This command is used to pull any image from official [docker hub](https://hub.docker.com/). by default, it pulls the latest image, but we can also mention the version of the image.

```
docker pull <imagekoname>
```

![][https://github.com/cybercena/Static-assets/blob/main/Docker/docker-pull.png?raw=true]

### Docker Ps
By default, this  command is used to shows us a list of all the running containers.  we can use different flags with it .
- **-a :** shows us all the containers, stopped or running.
- **-l :** shows us the latest container.
- **-q :** shows only the ID of the containers.

```
docker ps [options]
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/docker-ps.png?raw=true)

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerps-a.png?raw=true)

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerps-l.png?raw=true)

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerps-q.png?raw=true)

### Docker Stop
This command allows you to stop a container .

```
docker stop <container_id>
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerstop.png?raw=true)

### Docker Start
This command is used to run the existing container that is stopped accidentally or intentionally before.

```
docker start <container_id>
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerstart.png?raw=true)

### Docker rm
This command is used to delete a container. by default when  we create a container, it gets an ID and imaginary name or the name we have given such as practical_booth, homelab etc.
we need to mention the container name or ID to delete the container. we have various options for deleting container and they are :
- **-f :** remove the container forcefully
- **-v :** remove the volumes
- **-l :** remove the specific link mentioned

```
docker rm {options} <container_name or ID>
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerrmid.png?raw=true)

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerrmname.png?raw=true)

### Docker rmi
we can use this command to delete the images which are useless from the docker local storage and save spaces
```
docker rmi <image-id or name>
```

![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerrmi.png?raw=true)

![changes after removing images](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerrmichanges.png?raw=true)


### Docker images
 To lists all the pulled images present in our system we can use ``docker images`` command.

```
docker images
```
 
![](https://github.com/cybercena/Static-assets/blob/main/Docker/dockerimages.png?raw=true)
