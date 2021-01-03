---
title: gitpage 从笔记到博客
date: 2019-09-08 13:46:38
cover:
tags:
  - blog
---

## 读前准备
- [x] node install
- [x] hexo project
- [ ] hexo-generator-feed
- [x] hexo-deployer-git

<!-- more -->

### 创建 GitPage 仓库

登录 GitHub,在相关位置输入上文记录的内容。[登录地址](https://github.com/login)

![GitHub 登录界面](/img/blog/2.png)

如图所示，新建仓库，输入相关信息。仓库名（用户名.github.io）为 GitPage 固定写法。[新建仓库地址](https://github.com/new)

![仓库创建界面](/img/gitpage/2.png)

### 配置config

```diff
# _config.yml
- type
+ - type: git
+   repo: git@github.com:DukeBode/DukeBode.github.io.git
+   branch: master
```

![config配置](/img/gitpage/4.png)

git
- install

GitHub
- 账户
- ssh 免密访问

gitpage
- gitpage 仓库

analytics
- confing

search









