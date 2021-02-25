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

```ps1
# 检查程序版本，确认所需程序存在。
node -v; git version; npm -v; npx -v
# 创建并切换到工作目录
mkdir blog; cd blog
# 初始化 项目，git 仓库
npx hexo init; git init
# rss,sitemap
npm install hexo-generator-feed hexo-generator-sitemap hexo-deployer-git
# 创建CNAME,404,README
cd source
"" > CNAME
"---" >> 404.md; "permalink: /404.html" >> 404.md; "---" >> 404.md
"" > README.md
cd ../
# 创建项目简介
""> README.md
# 为项目建立捐助方式
mkdir .github;cd .github;"custom: ['https://DukeBode.github.io/sponsor']" > FUNDING.yml;cd ../
# 安装 hexo-theme-next 主题
npm install hexo-theme-next; cp node_modules/hexo-theme-next/_config.yml _config.next.yml
npm uninstall hexo-theme-landscape
# 别名 hexo
# 安装 npm scripts 依赖
npm install hexo-cli
```

## FAQ 
- [Set-ExecutionPolicy](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.core/about/about_execution_policies#change-the-execution-policy)
- 