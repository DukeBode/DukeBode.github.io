---
title: Linux
date: 2019-07-29 15:13:22
cover:
tags: FAQ
---

Linux Frequently Asked Questions

<!-- more -->

# yum

查看yum源Java包
yum list *java*

## Linux 基础

[文件目录](#文件目录)


使用nohup 和 & 让命令后台执行
---
- https://www.cnblogs.com/jinxiao-pu/p/9131057.html
- [Linux nohup实现后台运行程序及查看（nohup与&）](https://www.jb51.net/article/169783.htm)

[在RHEL 8/CentOS 8上安装LEMP（Nginx、MariaDB、PHP7.2）的方法](https://ywnz.com/linuxyffq/4544.html)

https://opsx.alibaba.com/mirror/search?q=dnf&lang=zh-CN

## 文件目录

![目录结构](/img/linux/目录结构.png)

根目录|-|-
-|-|-
bin -> usr/bin | 存放二进制可执行文件(ls,cat,mkdir等)，常用命令 普通用户命令
boot | 系统启动相关文件
dev | 设备文件
etc | 存放系统管理和配置文件
home | 普通用户家目录 存放所有用户文件的根目录，是用户主目录的基点
lib -> usr/lib | 系统库文件 存放着和系统运行相关的库文件
lib64 -> usr/lib64 | 
media | 媒介目录
mnt | 临时挂载目录 系统管理员安装临时文件系统的安装点，系统提供这个目录是让用户临时挂载其他的文件系统；
proc | 虚拟文件系统目录，是系统内存的映射。可直接访问这个目录来获取系统信息；
root | root的Home
run | 临时文件
sbin -> usr/sbin | root用户命令
srv | 服务产生文件
sys | 系统内核
tmp | 临时目录，用于存放各种临时文件，是公用的临时文件存储点；
usr | 程序目录
var | 存放日志 用于存放运行时需要改变数据的文件，也是某些大文件的溢出区，比方说各种服务的日志文件（系统启动日志等。）等

- /lost+found 这个目录平时是空的，系统非正常关机而留下“无家可归”的文件（windows下叫什么.chk）就在这里。
- /opt 额外安装的可选应用程序包所放置的位置。一般情况下，我们可以把tomcat等都安装到这里；
- /proc 系统启动的进程文件
  - Linux 内核的窗口，只存在于内存中，并不占用磁盘空间
  - 进程信息：进程项、进程参数列表、进程环境、进程可执行文件、进程文件描述符、进程内存统计信息等
  - 硬件信息：CPU信息、设备信息、PCI总线信息、串口信息等
  - 内核信息：版本信息、主机名与与域名信息、内存使用等
  - 设备、挂载点与文件系统 

## Linux Setting

### DNF

```sh
# /etc/yum.repos.d/dnf.repo
wget https://mirrors.aliyun.com/centos/7.5.1804/extras/x86_64/Packages/centos-release-yum4-1-2.el7.centos.noarch.rpm
yum install centos-release-yum4-1-2.el7.centos.noarch.rpm

# install DNF
yum install dnf
dnf upgrade
```

```sh
dnf -y groupinstall "Development Tools"
dnf -y install bzip2-devel sqlite-devel readline-devel libffi-devel systemtap-sdt-devel openssl-static  lzma tk-devel xz-devel  ncurses-devel gdbm-devel  gcc
# zlib 实现 gzip 压缩解压缩功能
# pcre 实现配置文件里的正则表达式解析功能
# openssl 实现 SSL 功能
dnf -y install zlib zlib-devel openssl openssl-devel pcre pcre-devel
```

## 文件校验
linux

md5sum hero.png 
fefd01c9db6e3e83b978eff1b7a67c02  hero.png
 
sha1sum hero.png 
f1e929db9cef34a8786ee4b6246fb739566c799d  hero.png
 
sha256sum hero.png 
5b654b2297f17d9106388db31c1190240cfb359144925e892468b40d692c780f  hero.png
 

windows

E:\>certutil -hashfile hero.png md5
MD5 哈希(文件 hero.png):
fefd01c9db6e3e83b978eff1b7a67c02
CertUtil: -hashfile 命令成功完成。
 

E:\>certutil -hashfile hero.png SHA1
SHA1 哈希(文件 hero.png):
f1e929db9cef34a8786ee4b6246fb739566c799d
CertUtil: -hashfile 命令成功完成。
 

E:\>certutil -hashfile hero.png SHA256
SHA256 哈希(文件 hero.png):
5b654b2297f17d9106388db31c1190240cfb359144925e892468b40d692c780f
CertUtil: -hashfile 命令成功完成。