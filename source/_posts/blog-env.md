---
title: 博客环境，让我们专注写笔记
date: 2019-09-08 15:22:37
cover:
tags:
  - blog
---


| [NodeJS 官网](https://nodejs.org) 
| [yarn 官网](https://yarnpkg.com) 
| [git 官网](https://git-scm.com/) 
| [VScode 官网](https://code.visualstudio.com/)

<!-- more -->

```sh
curl https://mirrors.huaweicloud.com/nodejs/v10.16.3/node-v10.16.3-win-x64.zip

https://mirrors.huaweicloud.com/yarn/v1.17.3/yarn-1.17.3.msi
$git='2.23.0';curl ('https://mirrors.huaweicloud.com/git-for-windows/v'+$git+'.windows.1/MinGit-'+$git+'-64-bit.zip') -o ('MinGit-'+$git+'-64-bit.zip')
```

- hexo 

- docusaurus

```sh
yarn global add docusaurus-init
```

1. 安装 node、yarn、git、vscode
1. yarn global add hexo-cli
1. hexo init blog

1. 配置 git 本地配置
1. 配置 github 用户 ssh
1. ssh -T git@github.com
1. 创建`用户名.github.io`仓库
1. git clone `git@github.com:用户名/用户名.github.io.git`
1. 将 blog 中所有文件移动至 `用户名.github.io`文件夹中
1. 配置 config 中的 deploy 参数
1. hexo -d
1. git pull



[hexo 官网](https://hexo.io/)

## 软件/插件

[NodeJS 官网](https://nodejs.org) | 
[VSCode 官网](https://code.visualstudio.com/) | 
[VSCode 中文插件](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans) |
[VSCode Hexo 插件](https://marketplace.visualstudio.com/items?itemName=codeyu.vscode-hexo)

- 依次到相应官网下载相应软件并自行安装
- 插件安装时需要打开 VScode
- shell 执行 
`npm install hexo-cli -g` 命令安装  hexo-cli

## 记事本
首行 .LOG