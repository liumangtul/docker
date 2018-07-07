# DOCKER #
## Quick Start ##

### login ###
docker login 

docker登陆账号 - 注意这里是账号不是注册的邮箱名

登录之后才可以进行docker的进一步操作

### Images ###

#### 搜索镜像 ####
docker search centos | grep centos

#### 查看本地镜像 ####
docker images

docker pull centos

等待，等待，等待


### container ###

#### 创建运行容器 ####
docker run centos /bin/echo 'hello docker'
docker run centos ls #创建运行，并输出该容器目录

创建并运行greeting容器
docker run centos --name greeting  /bin/echo 'hello docker'

run命令结束，容器及关闭

#### 管理容器 ####
docker ps --all
docker ps -a

docker rm container-name(id) #删除容器

docker logs container-name(id) #查看容器log

docker stop container-name(id) #停止容器

docker restart container-name(id) #重启容器

docker start container-name(id) #运行容器


### 进入容器并操作 ###
docker run --interactive --tty centos /bin/bash
--interactive 简写 -i
--tty         简写 -t

interactive 使用可交互的容器 

tty 给容器附加一个终端

centos 镜像名称

/bin/bash 终端位置

```
[root@1ea87419b2b7 /]#
    #1ea87419b2b7 主机名 使用的是container-id
    #接下来我们安装配置一些该容器内的应用

```

#### 后台运行容器 ###
docker run --detach --name wang  centos ping baidu.com

创建容器wang这，并在后台运行，执行ping 命令

docker logs --follow 62b4f21b300d #查看container-id的日志


