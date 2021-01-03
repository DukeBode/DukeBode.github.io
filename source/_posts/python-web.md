---
title: Python Web
date: 2020-02-06 12:55:04
cover:
tags: FAQ
---

Python Web Frequently Asked Questions

<!-- more -->


- [weppy](https://weppy.org/)

## 模板

模板|pip|page
-|-|-
[Mako](https://www.makotemplates.org/)|`pip install Mako` |[Docs](https://docs.makotemplates.org/en/latest/)
[mustache](https://mustache.github.io/)||


flask 基础操作
---
- [Flask中request请求、make_response响应、redirect跳转](https://www.jianshu.com/p/44d88abb9515)

flask 的request.full_path当链接无参数时末尾会自动添加一个?
---

uwsgi 下载
---
- https://uwsgi-docs.readthedocs.io/en/latest/Download.html
- https://uwsgi-docs.readthedocs.io/en/latest/Install.html
- https://uwsgi-docs.readthedocs.io/en/latest/WSGIquickstart.html

uwsgi部署flask测试
---
- https://flask.palletsprojects.com/en/1.1.x/deploying/wsgi-standalone/#uwsgi
- https://flask.palletsprojects.com/en/1.1.x/deploying/uwsgi/

部署测试，uwsgi 中 http、http-socket、socket 区别，unix套字节
---
- https://www.cnblogs.com/BlueFire-py/p/11381494.html?tdsourcetag=s_pctim_aiomsg

uwsgi 中 root 部署，指定uid、gid、chmod-socket
---
- https://www.cnblogs.com/BlueFire-py/p/11381494.html?tdsourcetag=s_pctim_aiomsg

nginx 配置
---
- https://www.cnblogs.com/BlueFire-py/p/11380439.html

nginx 通过 uwsgi 部署 flask
---
- http://www.pythondoc.com/flask/deploying/uwsgi.html#nginx
- https://www.missshi.cn/api/view/blog/5b1511a213d85b1251000000
- https://www.jianshu.com/p/76b28c7e71cc
- https://my.oschina.net/zhaojunhui/blog/3045805?tdsourcetag=s_pctim_aiomsg

nginx 部署后 链接中的//会自动变为一个/
---
- https://blog.csdn.net/github_33644920/article/details/52914932

uwsgi systemctl
---
- https://uwsgi-docs-zh.readthedocs.io/zh_CN/latest/Emperor.html?tdsourcetag=s_pctim_aiomsg
- https://uwsgi-docs-zh.readthedocs.io/zh_CN/latest/Systemd.html