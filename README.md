# 用docker-compose 搭建PHP开发环境

## 安装

docker-compose up -d

## 目录介绍

code目录用来存放你的项目代码


## 容器操作

### 访问容器
docker exec -it <container_id> bash

### 进入MySQL执行
docker exec -it <container_id> bash -l, 进入后就可以使用mysql命令连接数据库了.

mysql -u root -p root

### 监控
docker stats 监控容器状态