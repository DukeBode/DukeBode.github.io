---
title: init
date: 2021-02-19 19:46:39
tags:
---
<!-- more -->

# about_execution_policies

```ps1
Get-ExecutionPolicy
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

```
# rss,sitemap
npm install hexo-generator-feed hexo-generator-sitemap hexo-deployer-git
cd ../
# 创建项目简介
""> README.md
# 为项目建立捐助方式
mkdir .github;cd .github;"custom: ['https://DukeBode.github.io/sponsor']" > FUNDING.yml;cd ../
# 安装 hexo-theme-next 主题
npm install hexo-theme-next; 
cp node_modules/hexo-theme-next/_config.yml _config.next.yml
npm uninstall hexo-theme-landscape
# 别名 hexo

```

## 1. FAQ 
- [Set-ExecutionPolicy](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.core/about/about_execution_policies#change-the-execution-policy)
- 