---
title: Docker常用指令
description:  Docker常用指令
date: 2022-06-09T20:12:52+08:00
lastmod: 2022-06-09T20:12:52+08:00
tags:
  - Docker
  - Linux
categories:
  - Docker
draft: false
---

当然可以！以下是一些常用的 Docker 指令及其简要说明，供你参考：

### Docker 基本命令

1. **查看 Docker 版本**
   ```bash
   docker --version
   ```

2. **拉取镜像**
   ```bash
   docker pull <image_name>:<tag>
   ```
   示例：`docker pull ubuntu:latest`

3. **查看本地镜像**
   ```bash
   docker images
   ```

4. **删除镜像**
   ```bash
   docker rmi <image_id_or_name>
   ```

5. **查看运行中的容器**
   ```bash
   docker ps
   ```

6. **查看所有容器（包括已停止的）**
   ```bash
   docker ps -a
   ```

7. **启动容器**
   ```bash
   docker run <options> <image_name>
   ```
   示例：`docker run -d -p 80:80 nginx`

8. **停止容器**
   ```bash
   docker stop <container_id_or_name>
   ```

9. **启动已停止的容器**
   ```bash
   docker start <container_id_or_name>
   ```

10. **重启容器**
    ```bash
    docker restart <container_id_or_name>
    ```

11. **查看容器的日志**
    ```bash
    docker logs <container_id_or_name>
    ```

12. **进入正在运行的容器**
    ```bash
    docker exec -it <container_id_or_name> /bin/bash
    ```

13. **删除停止的容器**
    ```bash
    docker rm <container_id_or_name>
    ```

14. **构建镜像**
    ```bash
    docker build -t <image_name>:<tag> <path>
    ```
    示例：`docker build -t myapp:latest .`

15. **保存镜像到文件**
    ```bash
    docker save -o <output_file>.tar <image_name>
    ```

16. **从文件载入镜像**
    ```bash
    docker load -i <input_file>.tar
    ```

### Docker 网络管理

1. **查看网络**
   ```bash
   docker network ls
   ```

2. **创建网络**
   ```bash
   docker network create <network_name>
   ```

3. **删除网络**
   ```bash
   docker network rm <network_name>
   ```

### Docker 卷管理

1. **查看卷**
   ```bash
   docker volume ls
   ```

2. **创建卷**
   ```bash
   docker volume create <volume_name>
   ```

3. **删除卷**
   ```bash
   docker volume rm <volume_name>
   ```

### Docker Compose 相关命令

1. **启动服务**
   ```bash
   docker-compose up
   ```

2. **后台运行服务**
   ```bash
   docker-compose up -d
   ```

3. **停止服务**
   ```bash
   docker-compose down
   ```

4. **查看服务状态**
   ```bash
   docker-compose ps
   ```

这些是 Docker 中一些常见的操作指令。根据实际需要，你可能会使用到其中的部分或全部命令。如果你有特定的操作或问题，随时问我！
