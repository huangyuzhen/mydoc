# Container, 容器

## 命令

`docker container ls`

`docker container ls -a`

`docker container stop 1fa4ab2cf395`

```sh
docker container ls                                # List all running containers
docker container ls -a             # List all containers, even those not running
docker container stop <hash>           # Gracefully stop the specified container
docker container kill <hash>         # Force shutdown of the specified container
docker container rm <hash>        # Remove specified container from this machine
docker container rm $(docker container ls -a -q)         # Remove all containers
```