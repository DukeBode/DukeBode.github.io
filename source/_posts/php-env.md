---
title: CentOS 下安装 PHP7 
date: 2019-07-08 15:49:14
tags: 
- php
---

PHP Frequently Asked Questions

<!-- more -->

## 环境说明

- CentOS 7

## 源码安装 libiconv

[官网](http://www.gnu.org/software/libiconv/)

```sh
# 切换至程序源代码目录
cd /usr/src
# 下载 libiconv
wget https://ftp.gnu.org/pub/gnu/libiconv/libiconv-1.16.tar.gz
# 解压
tar -zxvf libiconv-1.16.tar.gz 
# 配置
./configure --prefix=/usr/local/libiconv
# 编译并安装
make && make install
```

## 源码安装 php7

[官网](https://www.php.net/)

```sh
# 切换至程序源代码目录
cd /usr/src
# 删除旧版本
rm -rf php-7.*
# 下载 php
wget https://www.php.net/distributions/php-7.3.8.tar.gz
# 解压
tar -zxvf php-7.3.8.tar.gz
# 删除压缩包
rm php-7.3.8.tar.gz
# 切换至 php 目录
cd php-7.3.8
# 配置 makefile 脚本
./configure
--prefix=/usr/local/php # 程序目录
--with-iconv=/usr/local/libiconv
--enable-fpm # fastcgi 方式运行
--with-pdo-mysql # mysql 数据库
--with-curl
--with-zlib
```

脚本配置成功

![脚本配置成功界面](/img/php/1.png)

```sh
# make 检查，可省略
make test
# 杀死全部 php-fpm 进程
killall php-fpm
# 编译并安装
make && make install
# 切换 php 目录
cd /usr/local/php/
# 复制 php.ini 配置文件
cp /usr/src/php-7.3.8/php.ini-production lib/php.ini
# 复制 nginx 配置文件
cp etc/php-fpm.conf.default etc/php-fpm.conf
# 复制配置文件
cp etc/php-fpm.d/www.conf.default etc/php-fpm.d/www.conf
# 启动php-fpm
./sbin/php-fpm
# 确认php-fpm成功
ps aux | grep php
# 查看占用端口
netstat -anpo | grep php
```

### phpinfo.php

```php
<?php
    phpinfo();
?>
```

#### nginx.conf

```nginx
location ~ \.php$ {
  root /www/php; #指定php的根目录
  fastcgi_pass 127.0.0.1:9000;#php-fpm的默认端口是9000
  fastcgi_index index.php;
  fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
  include fastcgi_params;
}
```

## 配置 php 模块

```sh
# 查看当前已加载模块
/usr/local/php/bin/php -m
# 切换至相应的模块源码目录
cd /usr/src/php-7.3.8/ext/curl/
#  设置软链接，防止头文件找不到的问题（类似问题同解）
ln -s /usr/src/php-7.3.8/ext/ ./ext
# 执行 phpize
/usr/local/php/bin/phpize
# 配置
./configure -with-php-config=/usr/local/php/bin/php-config
# 编译
make && make install
# 查看对应的 so 文件
ls /usr/local/php/lib/php/extensions/no-debug-non-zts-20180731/
# 编辑配置文件，可通过 phpinfo 函数查找文件位置
vi /usr/local/php/lib/php.ini
# 重启 php
/usr/local/php/sbin/php-fpm restart
```

编译安装可指定php.ini的路劲(多PHP版本共存的情况)
--with-config-file-path=/usr/local/php/etc

## 配置文件



---
- wget 的使用
- tar 的使用
- configure 的使用
- make 的使用

-----

./configure
--prefix=/usr/local/php --with-iconv=/usr/local/libiconv --enable-fpm --with-pdo-mysql 