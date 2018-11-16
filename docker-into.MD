## Docker使用介绍

进行某个container

docker exec -it <container_id> bash

实例化镜像运行并进入

docker run -it --rm <image_id> bash

删除停止运行的进程

docker-compose rm -v

一些参考的URL

[http://ctankersley.com/2016/07/27/my-php-docker-workflow/](http://ctankersley.com/2016/07/27/my-php-docker-workflow/)

[https://x-team.com/blog/docker-compose-php-environment-from-scratch/](https://x-team.com/blog/docker-compose-php-environment-from-scratch/)

[https://stackoverflow.com/questions/39657058/installing-gd-in-docker](https://stackoverflow.com/questions/39657058/installing-gd-in-docker)

[https://stackoverflow.com/questions/30063907/using-docker-compose-how-to-execute-multiple-commands](https://stackoverflow.com/questions/30063907/using-docker-compose-how-to-execute-multiple-commands)