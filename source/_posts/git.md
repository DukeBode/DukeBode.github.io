---
title: git 仓库配置
date: 2019-08-15 14:57:42
cover:
tags:
- git
---

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

<!-- more -->

## 常用 Git 仓库

腾讯工蜂 https://git.code.tencent.com

## git

![git 官网](/img/git/0.png)

[官网](https://git-scm.com/) | [中国下载](https://github.com/waylau/git-for-win)

## 安装 git

蝈蝈强烈要求读者，先读下文，然后再碰安装包。

### 中国用户问题

中国地区的 Window 宝宝请访问中国下载地址，最新日期的第一个链接即可

![git 下载页面](/img/blog/5.png)

### path 环境变量问题

安装的时候，为了方便以后操作，下面的修改环境变量操作选第二个，其它操作建议选择默认。

![git 安装界面](/img/git/4.png)

## shell 操作

1. 点击 `Windows + R` 打开在运行界面
1. 输入powershell 后，打开powershell

![运行 cmd](/img/git/11.png)

在弹出的软件中输入`git version`,回车查看 git 版本，确认安装成功

![验证 git 安装](/img/git/12.png)

确认成功安装后，依次输入以下命令回车执行，使用前面记录的信息替换相关内容，全程一律回车，直到执行完毕。

## 设置 git

```sh
# 查看 git 版本
git version
# 设置 git 全局用户名
git config --global user.name "DukeBode"
# 设置 git 全局邮箱
git config --global user.email Duke123@aliyun.com
```

## 创建本地仓库
```sh
git init  # 初始化仓库
git add * # 添加全部文件
```

## 配置远程仓库

git remote add origin git@。。。。。。。。。。。。。。。
git push -u origin --all

## 配置 SSH-Key

### 生成密钥对

```sh
# 格式 
# ssh-keygen -t rsa -C "通常为邮箱" -f "私钥文件绝对路径"
ssh-keygen -t rsa -C "Duke123@aliyun.com" -f "C:\Users\Duke1\.ssh\github"
```

### 配置 ssh config 文件

模板

```
# 仓库名
# 仓库地址
Host 仓库 git 地址
Host 仓库 git 地址
PreferredAuthentications publickey
IdentityFile 私钥文件绝对路径
```

config
[config](/config/ssh/config)
```
# github
# https://github.com/
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile C:\Users\Duke1\.ssh\github
```
```sh
git -T git@github.com
```

## 参考文章

1. [Git命令备份](https://www.jianshu.com/p/dbb352ea14cf)
1. [Git配置多个SSH-Key](https://gitee.com/help/articles/4229)
1. [aliyun SSH-Key](https://code.aliyun.com/help/ssh/README)
1. [在Windows下配置多个git账号](https://www.cnblogs.com/liuguanglin/p/8351616.html)
1. [Linux下安装Git](https://blog.csdn.net/sinat_29963957/article/details/81256227)
1. [CentOS安装GIT](https://www.cnblogs.com/sahara/p/5683066.html)
