---
title: System Variables Path
date: 2020-02-19 12:25:32
cover:
tags:
---

The PATH variable makes it easy to run commonly used programs located in their own folders. If used unwisely, however, the value of the PATH variable can slow down the operating system by searching too many locations, or invalid locations.

<!-- more -->

## 1. Linux 命令

1. date 时间
1. useradd 用户添加
1. whoami 当前登录用户
1. chmod -R 777 dirname 将dirname授权给所有用户
1. echo $PS1 显示提示符格式
1. ls 深蓝色：文件夹/目录 点开头：隐藏文件
1. ls -a
1. alias 起别名
1. type -a 查看本质

! 调用历史

### 1.1. 设置 path

`.profile` 记录了 bash 会在哪些目录查找命令。 bash 会根据 PATH 变量的设置自动寻找输入的命令。如果有同名的命令，按照路径顺序找到后返回执行，不再继续寻找。有同名的指令可以输入路径运行。

默认的路径：
```txt
~/bin
~/.local/bin
/usr/local/sbin
/usr/local/bin
/usr/sbin
/usr/bin
/sbin
/bin
/usr/games
/usr/local/games
```


### 1.2. 设置 path

```cmd
$Env:path="./.venv/Scripts/;"+$Env:path
```