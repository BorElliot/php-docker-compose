# 用docker-compose 搭建PHP开发环境

## v1版本
这个版本只包含简单的PHP环境，不包括安装扩展。

## v2版本
这个版本包含了PHP一些基本的扩展安装，它通过引入另一个dockerfile的方式来安装PHP扩展

可参考docker官方文档 [https://docs.docker.com/samples/library/php/#how-to-install-more-php-extensions](https://docs.docker.com/samples/library/php/#how-to-install-more-php-extensions)

## v3版本
这个版本也是在v1基础的增强，它通知command的方式来安装PHP扩展， 未经过实际测试。



## 安装

docker-compose up -d

## 目录介绍

code目录用来存放你的项目代码


## 容器操作

### 访问容器
docker exec -it <container_id> bash

重启容器
docker restart <container_id>

### 进入MySQL执行
docker exec -it <container_id> bash -l, 进入后就可以使用mysql命令连接数据库了.

mysql -u root -p root

### 监控
docker stats 监控容器状态

## 问题

composer遇到exited with code 127的时候，需要检查你是否是已root用户运行，是否是内存不够导致的，可以使用docker stats监控进程状态，如果内存不够就添加虚拟内存来解决。

`docker-compose up`在第一次运行完之后，下次再运行的话如果你更改了dockerfile的配置，需要把第一次生成的镜像删除，否则该镜像不会更新，并按照之前的镜像生成container。所以如果你更新了dockerfile，需要把之前生成的镜像删掉再重新运行`docker-compose up`