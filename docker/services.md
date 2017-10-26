# Service

## `docker-compose.yml`

```yml
version: "3"
services:
  web:
    # replace username/repo:tag with your name and image details
    image: username/repo:tag
    deploy:
      replicas: 5
      resources:
        limits:
          cpus: "0.1"
          memory: 50M
      restart_policy:
        condition: on-failure
    ports:
      - "80:80"
    networks:
      - webnet
networks:
  webnet:
```

```bash
docker swarm init
docker stack deploy -c docker-compose.yml getstartedlab
```

### 查看

### 列出service

`docker service ls`

### 查看service

`docker service ps <service>`

### 查看一个service的task

`docker inspect --format='{{.Status.ContainerStatus.ContainerID}}' <task>`

### 列出 container

`docker container ls -q`

### 重新加载

`docker stack deploy -c docker-compose.yml getstartedlab`

### 停止service

`docker stack rm getstartedlab`

### 停止swarm

`docker swarm leave --force`

```sh
docker stack ls                                            # List stacks or apps
docker stack deploy -c <composefile> <appname>  # Run the specified Compose file
docker service ls                 # List running services associated with an app
docker service ps <service>                  # List tasks associated with an app
docker inspect <task or container>                   # Inspect task or container
docker container ls -q                                      # List container IDs
docker stack rm <appname>                             # Tear down an application
docker swarm leave --force      # Take down a single node swarm from the manager
```