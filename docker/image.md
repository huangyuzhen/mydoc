# Images

镜像

``docker images``

``docker image ls``

``docker pull username/xx``

```sh
docker image ls -a                             # List all images on this machine
docker image rm <image id>            # Remove specified image from this machine
docker image rm $(docker image ls -a -q)   # Remove all images from this machine
```