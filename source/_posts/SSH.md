---
title: SSH 配置
date: 2018-06-11 16:34:30
tags:
---

<!-- more -->

## 1. 口令登录

```sh
ssh [-p 22] [user@]host
```

说明：
- 默认端口22可省略
- 用户名与本地用户名相同时可省略

## 2. 公钥登录

    1. 生成公钥

```sh
# 格式 
# ssh-keygen -t rsa -C "通常为邮箱" -f "私钥文件绝对路径"
ssh-keygen
```

说明：
- 私钥口令 passphrase，若担心私钥的安全，设置一个
- 公钥 id_rsa.pub，私钥 id_rsa
    2. 复制公钥至主机
    
```sh
cat pub_file_path | ssh  root@host 'cat >> .ssh/authorized_keys'
# 首次登录使用，覆盖已有的 id_rsa 之后即可无密码登录，如果设置了 passphrase 登录时需要输入 passphrase
ssh-keygen; cat ~/.ssh/id_*.pub | ssh  root@host 'cat >> .ssh/authorized_keys'; ssh user@host
```

```config
host ecs（主机别名）
HostName 主机地址
User 用户名
Port 22（sshd 端口号）
IdentitiesOnly yes
IdentityFile 私钥路径
```

```conf

PermitRootLogin yes
```
