---
title: oracle
date: 2020-03-02 10:16:49
cover:
tags:
---

<!-- more -->
- [Database Software Downloads | Oracle](https://www.oracle.com/database/technologies/oracle-database-software-downloads.html)

- [Oracle Database Documentation - Oracle Database](https://docs.oracle.com/en/database/oracle/oracle-database/index.html)

- Oracle Enterprise Manager Database Express

https://localhost:5500/em

- lsnrctl 监听服务管理

```sh
# 查看运行状态
lsnrctl status
# 启动监听
lsnrctl start
# 关闭监听
lsnrctl stop
```

- sqlplus 

```sh
sqlplus -H
# 不登录
sqlplus /nolog
# 超级管理员
conn / as sysdba # 操作系统身份认证
conn sys as sysdba
# 普通管理员
conn system
# 普通用户(用户名无效)
conn scott
```

```sql plus
-- 启动实例并打开数据库
startup
-- 关闭实例
shutdown
-- 查看当前登录用户
show user;
-- 查看当前登录的用户信息
select * from user_users;
-- 查询用户
select username from dba_users;
-- 执行 sql 文件，导入 scott 用户
@oracle_installer_path\rdbms\admin\scott.sql
-- 解锁 scott 用户
alter user scott account unlock ; 
-- 设置 scott 用户的密码为 tiger
alter user scott identified by tiger;
```
