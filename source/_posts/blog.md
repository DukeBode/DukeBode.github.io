---
title: 零基础建博客
date: 2019-06-07 17:03:20
cover: /img/blog/1.png
tags:
- hexo
- VScode
- git
- nodejs
- GitHub
- GitPage
- 博客
---


### 0.1. Hexo 博客
Hexo 不是博客而是快速、简洁且高效的博客框架，适合任何有打字基础的人建立属于自己、完全定制的个人博客，可用于个人生活记录、学习笔记整理、连载个人小说等。

<!-- more -->

[hexo](hexo) 

---
### 0.2. 流程简介
- 前期准备：申请 GitHub 账户、创建 GitPage 仓库、配置 Git 环境、配置 Nodejs 环境
- 搭建博客：安装 Hexo-cli、搭建博客环境、设置博客主题、部署博客至 GitPage
- 博客编写：Hexo 命令、安装 VScode 插件、Markdown 编写博客
---

### 0.3. 申请 GitHub 账户

访问 GitHub 官网 建立自己的 GitHub 帐号：[注册地址](https://github.com/join)

### 0.4. 创建 GitPage 仓库

登录 GitHub,在相关位置输入上文记录的内容。[登录地址](https://github.com/login)

![GitHub 登录界面](/img/blog/2.png)

如图所示，新建仓库，输入相关信息。仓库名（用户名.github.io）为 GitPage 固定写法。[新建仓库地址](https://github.com/new)

![仓库创建界面](/img/blog/3.png)

说明：
`黄色标记`会自动显示对应的个人信息，`绿色标记`需要自己填写，填写时请勿遗漏点等字母或符号。

### 0.5. 配置 Git 环境

不是`中国地区`的` Windows 系统`用户请自行阅读官网文档安装，切记配置 path 环境。 [git 官方下载地址](https://git-scm.com/downloads)

### 0.6. 配置 Nodejs 环境

[NodeJS 官网]()

git clone -b <指定分支名> <远程仓库地址>

### 0.7. 编写博客

```bat
set PATH=%PATH%;
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Environment" /v "Path" /t REG_EXPAND_SZ /d "%PATH%" /f
```

> 参考文章 
- [hexo搭建个人博客](https://blog.csdn.net/lucklymm/article/details/89014085)


用电脑记笔记
让更多人看到自己的笔记
备份笔记