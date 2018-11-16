## Docker使用介绍

进行某个container

docker exec -it <container_id> bash

实例化镜像运行并进入

docker run -it --rm <image_id> bash

删除停止运行的进程

docker-compose rm -v