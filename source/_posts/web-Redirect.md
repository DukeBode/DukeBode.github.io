---
title: web-Redirect
date: 2021-07-26 09:10:27
tags:
---
<!-- more -->
```html
<!DOCTYPE html>
<html>
<head>
    <!-- 避免缓存 -->
    <meta http-equiv="Pragma" content="no-cache">
    <meta http-equiv="Cache-Control" content="no-cache">
    <meta http-equiv="Expires" content="0">
    <title>Document</title>
    <script>
        location.href="http://www.baidu.com";
        location.replace("http://www.baidu.com")
    </script>
</head>
<body>
</body>
</html>
```

Ctrl + F5 强制刷新  