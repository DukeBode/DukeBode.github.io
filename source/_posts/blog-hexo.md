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

```sh
# 检查程序版本，确认所需程序存在。
node -v; 
git version; 
npm -v; 
npx -v
# 创建并切换到工作目录
mkdir blog
cd blog
```
## 1. 初始化博客环境

```sh
npx hexo init
```
## 2. 博客名称

`_config.yml`
```diff
-title: Hexo
+title: Duke Blog
```

## 3. 博客网址

`_config.yml`
```diff
-url: http://example.com
+url: https://DukeBode.github.io
```
## 4. 页面

`source/404.md`
```md
---
permalink: /404.html
---

[返回首页](/)
```

## 5. CNAME

`source/CNAME`


## 6. 主题设置

theme: duke

## 7. 部署至 GitPage


配置config

```diff
_config.yml

-  type
+  type: git
+  repo: git@github.com:DukeBode/DukeBode.github.io.git
+  branch: master
```

```sh
# 安装插件
yarn add hexo-deployer-git
# 部署
hexo d
```

## 8. git 备份

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

## 9. git 恢复

```sh
git clone -b backup git@github.com:DukeBode/DukeBode.github.io.git blog
```

## 10. 多机编写



## 11. 网站地图

> 为搜索引擎提供搜索依据

```sh
yarn add hexo-generator-sitemap
```

## 12. RSS 订阅

> 方便用户订阅

```sh
yarn add hexo-generator-feed
```

## 13. 评论

- gitalk

[](https://www.pengfeima.cn/posts/notes/1/)