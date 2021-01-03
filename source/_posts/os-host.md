---
title: os-host
date: 2020-02-24 10:48:19
cover:
tags:
---

The hosts file is one of several system facilities that assists in addressing network nodes in a computer network. It is a common part of an operating system's Internet Protocol (IP) implementation, and serves the function of translating human-friendly hostnames into numeric protocol addresses, called IP addresses, that identify and locate a host in an IP network.

<!-- more -->

系统 | host 文件路径
-|-
Windows  | C:\Windows\System32\drivers\etc\hosts
Linux/Mac | /etc/hosts

## 功能

- 加快域名解析
- 重定向恶意域名
- 虚拟域名

https://github.com/googlehosts/hosts


添加下面两行内容到hosts文件中

151.101.72.249 github.global.ssl.fastly.net

192.30.253.112 github.com