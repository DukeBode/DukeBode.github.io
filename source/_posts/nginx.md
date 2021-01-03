---
title: nginx
date: 2018-11-08 16:48:45
tags: 
- linux
- nginx
---

<!-- more -->

[官网](https://www.nginx.com/)

- expires

[Nginx设置expires设定页面缓存时间 不缓存或一直使用缓存](https://www.cnblogs.com/yuanzai12345/p/5946743.html)

# 版本简介

- Mainline 主线开发版本，版本号为奇数
- Stable   当前稳定版本，版本号为偶数
- Legacy   历年稳定版本

## 源码安装

```shell
# wget http://nginx.org/download/nginx-1.14.0.tar.gz
# tar -zxvf nginx-1.14.0.tar.gz
# cd nginx-1.14.0
# ./configure --with-http_ssl_module --with-http_v2_module
# make

```
```
Configuration summary
  + using system PCRE library
  + OpenSSL library is not used
  + using system zlib library

  nginx path prefix:          "/usr/local/nginx"
  nginx binary file:          "/usr/local/nginx/sbin/nginx"
  nginx modules path:         "/usr/local/nginx/modules"
  nginx configuration prefix: "/usr/local/nginx/conf"
  nginx configuration file:   "/usr/local/nginx/conf/nginx.conf"
  nginx pid file:             "/usr/local/nginx/logs/nginx.pid"
  nginx error log file:       "/usr/local/nginx/logs/error.log"
  nginx http access log file: "/usr/local/nginx/logs/access.log"
  nginx http client request body temporary files: "client_body_temp"
  nginx http proxy temporary files:   "proxy_temp"
  nginx http fastcgi temporary files: "fastcgi_temp"
  nginx http uwsgi temporary files:   "uwsgi_temp"
  nginx http scgi temporary files:    "scgi_temp"
  ```
## Nginx 操作命令
- nginx -s reload 重新加载配置文件
- nginx -s reopen 重新打开日志文件
- nginx -t        测试 nginx 配置文件是否正确
- nginx -t -c /path/to/nginx.conf 测试 nginx 配置文件是否正确
- nginx -s stop 快速停止 nginx

## 附：
>- NGINX 官网      www.nginx.org
>- NGINX docs      nginx.org/en/docs
>- NGINX configure nginx.org/en/docs/configure.html
>- tar 命令 man.linuxde.net/tartar