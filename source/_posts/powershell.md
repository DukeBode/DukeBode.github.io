---
title: PowerShell笔记
date: 2018-06-03 16:34:30
cover:
tags: shell
---

## shell 语法

- 变量声明以“$”开头后跟变量名
- 变量名不区分大小写，可包含数字、字母和下划线
- 预定义变量
- $null（空值）$true（真值为真）$false（真值为假）$_（当前处理的元素）

命令|含义
-|-
net share | 查看共享文件


## 脚本运行

### 运行权限
Windows 默认不允许任何脚本运行，可以使用"Set-ExecutionPolicy" cmdlet 来改变的你PowerShell环境。例如，你可以使用如下命令让PowerShell运行在无限制的环境之下：

```powershell
# 查看当前脚本运行权限
ExecutionPolicy
# 设置脚本运行权限，允许任何脚本运行
Set-ExecutionPolicy Unrestricted;
```

- Restricted——默认的设置， 不允许任何script运行
- AllSigned——只能运行经过数字证书签名的script
- RemoteSigned——运行本地的script不需要数字签名，但是运行从网络上下载的script就必须要有- 数字签名
- Unrestricted——允许所有的script运行

如果报错，使用管理员的权限启动命令命令行重试。

### java 调用脚本
使用 java 调用 powershell 脚本，可以使用以下命令：
```java
String cmd = "cmd /c powershell 
-ExecutionPolicy RemoteSigned -noprofile 
-noninteractive -file \""+ scriptFilename + "\"";
```