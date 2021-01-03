---
title: HEXO 进阶操作
date: 2019-09-22 14:49:12
cover:
tags:
  - blog
  - hexo
---

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

<!-- more -->

## 初始化博客环境

```sh
hexo init blog
```

## 404 页面

source 目录下新建 404.md 文件

```md
<script>
location.href="https://dukebode.github.io/";
</script>
```

## CNAME

source/CNAME

## 主题设置

theme: duke

## 部署至 GitPage

配置config

```diff
_config.yml
- type
+ - type: git
+   repo: git@github.com:DukeBode/DukeBode.github.io.git
+   branch: master
```

```sh
# 安装插件
yarn add hexo-deployer-git
# 部署
hexo d
```

## git 备份

我们将采用 gitpage 的 backup 分支来备份

```sh
# git 仓库
git init
# 添加文件
git add *
# 提交至版本库
git commit -m "hexo backup"
# 添加远程仓库
git remote add origin git@github.com:DukeBode/DukeBode.github.io.git
# 创建 backup 分支
git branch backup
# 切换 backup 分支
git checkout backup
# 删除 master 分支
git branch -d master
# 推送 backup 分支
git push -u origin backup
```

## git 恢复

```sh
git clone -b backup git@github.com:DukeBode/DukeBode.github.io.git blog
```

## 多机编写



## 网站地图

> 为搜索引擎提供搜索依据

```sh
yarn add hexo-generator-sitemap
```

## RSS 订阅

> 方便用户订阅

```sh
yarn add hexo-generator-feed
```

## 评论

- gitalk