---
title: ish
date: 2023-07-12 22:53:27
tags:
---

The Linux shell for iOS.

<!-- more -->

## 1. Alpline Linux

查看版本
```sh
cat /etc/os-release
cat /etc/alpine-release
```

配置源
```
/etc/apk/repositories
```repositories
https://mirrors.tuna.tsinghua.edu.cn/alpine/v3.14/community
https://mirrors.tuna.tsinghua.edu.cn/alpine/v3.14/main
```
异常处理

fatal error: stdio.h: No such file or directory
```sh
apk add musl-dev
```

clang: error: unable to execute command: Executable "ld" doesn't exist!
```sh
apk add binutils
```

## 2. 挂载


midair -p ~/obsidian
mount -t ios . obsidian
