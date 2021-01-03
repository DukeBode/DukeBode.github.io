---
title: php Web Server
date: 2019-07-31 18:26:44
cover:
tags:
- php
---

> PHP 5.4.0起， CLI SAPI 提供了一个内置的Web服务器。主要用于本地开发使用，不可用于线上产品环境。

<!-- more -->

## php Web Server

```sh
# 方式一，仅配置端口启动，以当前目录为服务器根目录
php -S localhost:8000
# 方式二，配置端口，并指定根目录
php -S localhost:8000 -t foo/
# 方式三，配置端口，调用路由（router）脚本
php -S localhost:8000 router.php
```

URI请求会被发送到PHP所在的的工作目录（Working Directory）进行处理，除非你使用了-t参数来自定义不同的目录。

如果请求未指定执行哪个PHP文件，则默认执行目录内的index.php 或者 index.html。如果这两个文件都不存在，服务器会返回404错误。

当你在命令行启动这个Web Server时，如果指定了一个PHP文件，则这个文件会作为一个“路由”脚本，意味着每次请求都会先执行这个脚本。如果这个脚本返回 FALSE ，那么直接返回请求的文件（例如请求静态文件不作任何处理）。否则会把输出返回到浏览器。

### router.php 示例代码

```php
<?php
// router.php
// 请求图片直接显示图片，请求HTML则显示“Welcome to PHP”
if (preg_match('/\.(?:png|jpg|jpeg|gif)$/', $_SERVER["REQUEST_URI"]))
    return false;    // 直接返回请求的文件
else { 
    echo "<p>Welcome to PHP</p>";
}
?>
```


> 参考文章 
- [内置Web Server](https://www.php.net/manual/zh/features.commandline.webserver.php)