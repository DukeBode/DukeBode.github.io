---
title: System Variables Path
date: 2020-02-19 12:25:32
cover:
tags:
---

The PATH variable makes it easy to run commonly used programs located in their own folders. If used unwisely, however, the value of the PATH variable can slow down the operating system by searching too many locations, or invalid locations.

<!-- more -->

## Linux 命令

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

### 设置 path

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

## Windows 运行常用的命令

命令|含义|备注
-|-|-
appwiz.cpl | 程序和功能 | 常用于卸载软件
logoff | 注销 | 注销计算机
shutdown | 60秒倒计时关机命令|
cmd | cmd | 命令提示符
calc | 计算器 |
cleanmgr | 磁盘清理 |
msconfig | 系统配置实用程序
osk | 屏幕键盘
psr | 步骤记录器|
snippingtool | 截图工具 | 已被截图和草图取代
winver | 关于"Windows" | 查看 Windows 版本
explorer | 资源管理器
regedit | 注册表编辑器
taskmgr | 任务管理器
compmgmt.msc | 计算机管理
devmgmt.msc | 设备管理器

### 设置 path

$Env:path="./.venv/Scripts/;"+$Env:path