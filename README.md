# Docker Alpine Redis

## 环境

```
alpine: ^3.11
redis: 5.0.7
```

## 常用命令：

```sh
# 拉取镜像
$ docker pull seffeng/redis

# 运行
$ docker run --name redis-test -d -v <data-dir>:/opt/websrv/data/redis -v <tmp-dir>:/opt/websrv/tmp seffeng/redis

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
