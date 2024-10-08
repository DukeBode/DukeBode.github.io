---
title: git 仓库配置
date: 2019-08-15 14:57:42
cover:
tags:
- git
---


Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

<!-- more -->

## 1. 常用 Git 仓库

腾讯工蜂 https://git.code.tencent.com
gitcode.com

## 2. git

[官网](https://git-scm.com/) | [中国下载](https://github.com/waylau/git-for-win)

## 3. 安装 git

蝈蝈强烈要求读者，先读下文，然后再碰安装包。

### 3.1. 中国用户问题

中国地区的 Window 宝宝请访问中国下载地址，最新日期的第一个链接即可

![git 下载页面](/img/blog/5.png)

### 3.2. path 环境变量问题

安装的时候，为了方便以后操作，下面的修改环境变量操作选第二个，其它操作建议选择默认。

![git 安装界面](/img/git/4.png)

## 4. shell 操作

1. 点击 `Windows + R` 打开在运行界面
1. 输入powershell 后，打开powershell

![运行 cmd](/img/git/11.png)

在弹出的软件中输入`git version`,回车查看 git 版本，确认安装成功

![验证 git 安装](/img/git/12.png)

确认成功安装后，依次输入以下命令回车执行，使用前面记录的信息替换相关内容，全程一律回车，直到执行完毕。

## 5. 设置 git

```sh
# 查看 git 版本
git version
# 设置 git 全局用户名
git config --global user.name "DukeBode"
# 设置 git 全局邮箱
git config --global user.email 29868250+DukeBode@users.noreply.github.com
# 设置 git 对比工具
git config --global diff.tool vimdiff
git config --global difftool.prompt false
```
## 6. 创建本地仓库
```sh
git init  # 初始化仓库
git add * # 添加全部文件
```

## 7. 配置远程仓库

git remote add origin git@。。。。。。。。。。。。。。。
git push -u origin --all

## 8. 配置 SSH-Key

### 8.1. 生成密钥对

```sh
# 格式 
# ssh-keygen -t rsa -C "通常为邮箱" -f "私钥文件绝对路径"
ssh-keygen -t ed25519 -C "giee.com" -f "~/.ssh/gitee"
ssh-keygen -t ed25519 -C "github.com" -f "~/.ssh/github"
ssh-keygen -t ed25519 -C "gitlab.com" -f "~/.ssh/gitlab"
ssh-keygen -t ed25519 -C "gitcode.com" -f "~/.ssh/gitcode"
```

### 8.2. 配置 ssh config 文件

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

```
# github
# https://github.com/
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~\.ssh\github
```

```sh
ssh -T git@github.com
```

## 9. git 撤销已经push的提交
- [git branch](https://git-scm.com/docs/git-branch) 查看分支
- [git log](https://git-scm.com/docs/git-log/) 查看提交日志
- [git reset](https://git-scm.com/docs/git-reset) 重置当前HEAD到指定的状态
- [git push](https://git-scm.com/docs/git-push)
1. git log

2. git reset --soft 

3. git push origin master --force
4. git clone --depth 1

## 10. 模块
```sh
# 添加默认分支
git submodule add url [path]
# 添加指定分支
git submodule add -b dev git@ip:src/name.git submodule_filename
# 更新 submodule 为远程项目的最新版本
git submodule update --remote
git clone url.git --recurse-submodules
```

```sh
README.md
LICENSE.txt
CTTATION.cff
.gitignore
CODE_OF_CONDUCT.md
# 参与者指南
CONTRIBUTING.md
GOVERNACE.md
# 安全政策
.github/SECURITY.md
.github/SUPPORT.md
.github/ISSUE_TEMPLATE/

.github/FUNDING.yml
# 代码所有者
.github/CODEOWNERS
# workflows
.github/workflows/

```


## 11. github 访问慢

mirrors - GitCode [https://gitcode.com/org/mirrors](https://gitcode.com/org/mirrors)

使用 gitcode 替代 github 访问源
使用 kkgithub 替换 github 在线访问下载

## 12. 参考文章

1. [Git命令备份](https://www.jianshu.com/p/dbb352ea14cf)
1. [Git配置多个SSH-Key](https://gitee.com/help/articles/4229)
1. [aliyun SSH-Key](https://code.aliyun.com/help/ssh/README)
1. [在Windows下配置多个git账号](https://www.cnblogs.com/liuguanglin/p/8351616.html)
1. [Linux下安装Git](https://blog.csdn.net/sinat_29963957/article/details/81256227)
1. [CentOS安装GIT](https://www.cnblogs.com/sahara/p/5683066.html)
3. [Git Submodule 使用](https://zhuanlan.zhihu.com/p/374662328)
4. [# git 本地仓库同时推送到多个远程仓库](https://fanfu.blog.csdn.net/article/details/79386169)
