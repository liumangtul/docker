# DOCKER #
## Quick Start ##

### login ###
docker login | logout

docker账号 - 注意这里是账号不是注册的邮箱名

登录之后才可以进行docker的进一步操作

____

### IMAGES ###

#### search images ####
docker search image-name | grep keyword

[docker hub](http://hub.docker.com "docker hub")

#### pull images ####
docker pull image-name

### CONTAINER ###

#### run container ####
docker run centos /bin/echo 'hello'
docker run --name container-name image-name /bin/echo 'hello'


docker run centos ls

#### view container ####
docker ps -all
docker ps -a -last
             -l 最后创建的容器

-a 显示所有容器，默认是running container

#### remove container ####
docker rm container-id(name)

#### controller container ####
docker stop container-name

docker start container

docker restart container

docker logs greeting # 查看容器日志

<font color=gray size=72>color=gray</font>


