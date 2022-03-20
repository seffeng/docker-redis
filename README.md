# Docker Alpine Redis

## 版本

* [6.2.6 , latest](https://github.com/seffeng/docker-redis/tree/6.2)
* [6.0.16](https://github.com/seffeng/docker-redis/tree/6.0)
* [5.0.14](https://github.com/seffeng/docker-redis/tree/5.0)

## 常用命令：

```sh
# 拉取镜像
$ docker pull seffeng/redis

# 运行
$ docker run --name redis-test -d -p <port>:6379 -v <data-dir>:/opt/websrv/data/redis -v <tmp-dir>:/opt/websrv/tmp seffeng/redis

# 例子：
$ docker run --name redis-alias1 -d -p 6379:6379 -v /opt/websrv/data/redis:/opt/websrv/data/redis -v /opt/websrv/tmp:/opt/websrv/tmp seffeng/redis

# 查看正在运行的容器
$ docker ps

# 停止
$ docker stop [CONTAINER ID | NAMES]

# 启动
$ docker start [CONTAINER ID | NAMES]

# 进入终端
$ docker exec -it [CONTAINER ID | NAMES] sh

# 删除容器
$ docker rm [CONTAINER ID | NAMES]

# 镜像列表查看
$ docker images

# 删除镜像
$ docker rmi [IMAGE ID]
```
#### 备注

```shell
# 建议容器之间使用网络互通
## 1、添加网络[已存在则跳过此步骤]
$ docker network create network-01

## 运行容器增加 --network network-01 --network-alias [name-net-alias]
$ docker run --name redis-alias1 --network network-01 --network-alias redis-alias1 -d -p 6379:6379 -v /opt/websrv/data/redis:/opt/websrv/data/redis -v /opt/websrv/tmp:/opt/websrv/tmp seffeng/redis
```