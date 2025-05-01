# basic concept

## 1. client and server
`systemctl start docker`

## 2. image
read only.
read layer.
### `podman images`
list local images.

### `podman image`

### `docker images`
show all local images

### `docker rmi hash`
delete local image

## 3. container
read and write

# common command
## ps
docker `container(could ignore)` ps `-al`

## ls

## support pipline

## attach and detach
use attach can entry the container.

## pull
pull remote image not containr.
You'd better to indicate your command 

## run
Run would build a new instance

## start
execute the same container

# docker-compose
## about installment
in windows it willbe installed by default.
In linux, you should manually install it.

# devContainer
the most useful app is dev container.
Try to look up the VScode article in this repo.

## pay attention to the right tag
select the proper tag for the image so that to satisfy the requirement of the project

## pay attention to the port forward policy
