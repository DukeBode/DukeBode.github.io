---
title: Django 部署
date: 2018-07-18 16:34:30
tags:
- python
- Django
- 框架
---

<!-- more -->

## 阅读基础
- [Python3 安装](Python3.md)

## 配置虚拟环境

> 表中命令从上往下执行即可，部分需要先切换目录，下同。本文为学习笔记，仅供参照，详细流程请阅读参考文章和官方文档。

||操作|命令|
|-|-|-|
|-|创建虚拟环境 | `python3 -m venv /www/venv`|
|-|激活虚拟环境 | `source /www/venv/bin/activate`|
|-|Windows下激活|`.\venv\Scripts\activate`|
|-|使用 uwsgi 部署| `pip install uwsgi`|
|-|使用 Gunicorn 部署| `pip install gunicorn`|
|-|安装环境包 | `pip install -r requirements`|
|-|生成环境包 | `pip freeze > requirements.txt`|
|-|退出环境 | `deactivate`|

## Django 项目开发
 
||操作|命令|备注
-|--|--|--
-|创建 django 项目 web | `django-admin startproject web`|生成项目目录
-|创建应用 count | `python manage.py startapp count` | 开发使用
-|创建超级账户 | `python manage.py createsuperuser` | 开发、部署使用
-|生成迁移文件 |`python manage.py makemigrations` | 在 migrations 生成文件
-|执行迁移 | `python manage.py migrate`
-|同步静态文件|`python manage.py collectstatic` | 部署使用
-|启动开发服务器|`python manage.py runserver` | 开发、测试使用

## 配置 setting`.`py

    - LANGUAGE_CODE = 'zh-Hans'
    - TIME_ZONE = 'Asia/Shanghai'（视情况配置）
    - ALLOWED_HOSTS = ['公网ip',域名']（部署前配置）
    - DEBUG = False（NGINX 后配置）

## 部署准备

    - 删除 migrations 下数字开头的所有 python 文件
    - uwsgi.ini
    ```ini
    [uwsgi]
    chdir = /www/web
    module = web.wsgi:applocation
    home = /www/venv
    socket = 172.18.173.33:8099
    stats = 172.18.173.33:9191
    master = true
    processes = 5
    vacuum = true
    ```

## 部署测试

    - 开发服务器测试 `python36 manage.py runserver 172.18.173.33:80`
    - uwsgi 部署测试 `uwsgi uwsgi.ini`
    - Gunicorn 部署测试 `gunicorn -b 172.18.173.33:80 web.wsgi`

## 配置 nginx

```
# 安装 uwsgi
pip3 install uwsgi
# 安装 nginx
yum install nginx
```

测试

nginx -t


## 参考文章 

- [Django+Ubuntu WEB部署（超详细版）](https://www.jianshu.com/p/e13417a8bb7f)
- [跨过Nginx上基于uWSGI部署Django项目的坑](https://www.cnblogs.com/qingspace/p/6838747.html)
- [Django快速部署简约版 v3.0](https://www.jianshu.com/p/d6f9138fab7b)