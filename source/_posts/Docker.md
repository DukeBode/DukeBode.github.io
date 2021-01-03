---
title: Docker
date: 2019-06-07 14:04:29
tags:
- 软件
---

<!-- more -->

# 部署 nginx
- 仓库查找镜像 `docker search nginx`
- 拉取官网镜像 `docker pull nginx`
- 查看本地镜像 `docker images`
- 启动所需容器 `docker run -d -p 80:80 nginx`
- 80端口打开