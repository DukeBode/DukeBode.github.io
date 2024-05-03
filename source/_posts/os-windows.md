---
title: Windows
date: 2020-03-24 13:55:33
cover: 
tags:
  - Windows
---

<!-- more -->
备忘录

- 选 管理员配置符号链接
```sh
# google C:\Program Files (x86)\Google
# C:\Program Files\Microsoft Office
# C:\Program Files\Microsoft Office 15
mklink /d 默认安装位置 用户指定的安装位置

New-Item -ItemType SymbolicLink -Path E:\DukePath\path3 -Target E:\DukePath\julia.lnk
```

文件类型|文件类型|路径|空间占用|适用类型| 特点
-|-|-|-|-|-
符号链接|  symlink| 可相对| 很小 | 文件| 可跨磁盘
符号链接| symlinkd| 可相对 |很小 | 目录| 可跨磁盘
目录联接 | junction| 绝对| 很小| 目录| 只能跨本地磁盘
硬链接 | 同源文件 | 绝对|与源文件大小相同 | 文件|不可跨分区
快捷方式 | lnk |绝对|几百字节，与源文件大小无关| 文件、目录、网站、命令| 仅人使用舒服

- Windows 10 环境下，删除任何链接均不会对源文件造成影响。
- 快捷方式可携带参数使用，程序读写一般是对快捷方式文件操作，而其它方式会直接对源文件操作，或同步操作至源文件。
- 符号链接使用相对路径会导致移动后失效，而其它方式则不会。
- 将源文件移除后，只有硬链接依然可以访问，其它方式则将失效。
- 相比快捷方式，使用符号链接尽管可以节约空间，但无法完全取代快捷方式。
- 符号链接多用于分离系统和软件分区，解除路径依赖、空间占用问题；整合 path 环境，便于系统的重装和维护。
- Windows操作系统启动时不支持符号链接。所以不应该对系统盘下系统目录、根目录的系统配置文件、隐藏文件进行操作。

Link    指定新的符号链接名称。

Target  指定新链接引用的路径
                (相对或绝对)。

cmd | [mklink](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/mklink)

```bat
rem 符号链接-文件
mklink Link Target
rem 符号链接-目录
mklink /d Link Target 
rem 目录联接
mklink /j Link Target
rem 硬链接
mklink /h Link Target
```

PowerShell | [new-item](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/new-item)

```powershell
# 符号链接
New-Item -ItemType SymbolicLink -Path Link -Target Target
# 目录联接
New-Item -ItemType Junction -Path Link -Target Target
# 硬链接
New-Item -ItemType HardLink -Path Link -Target Target
```


- 选 配置快捷键（带参数）

- 选 删除 OneDrive、自带游戏
- 选 配置打开文件资源管理器时打开此电脑
- 选 取消隐私选项
- 选 默认显示后缀名
- 选 关闭传递优化
- 配置用户文件路径
- 放置配置文件
- 配置 环境变量
- 更新驱动
- 选 安装 [wepe](http://www.wepe.com.cn/)
- 选 下载 [windows 10](https://www.microsoft.com/zh-cn/software-download/windows10)
- 更新 uwp 应用
- 安装/配置 压缩软件
- 安装 浏览器
- 选 关闭虚拟内存


## 1. 备份

- 环境变量 set path
- 配置文件 wifi、ssh、gradle
```sh
# 显示配置文件
netsh wlan show profile

# 导出 WiFi 文件
netsh wlan export profile folder=D:\ key=clear
```
- 软件安装包

[在Windows中启用和禁用触摸屏](https://support.microsoft.com/zh-cn/windows/在屏幕中启用和禁用触摸屏windows-b774e29d-be94-990f-c20f-e02892e572fc)

## 2. cmd命令的重定向输出

命令的结果可以通过“%>”的形式来定向输出，%表示文件描述符：1为标准输出stdout、2为标准错误stderr。系统默认%值是1，也就是“1>”，而1>可以简写为>，也就是默认为>。stdout的默认目标是终端，stderr的默认目标为也是终端。

来自 <[https://blog.csdn.net/earbao/article/details/51790405](https://blog.csdn.net/earbao/article/details/51790405)>

1、将结果输出到result.txt

net stop myservices >>result 2>&1

2、隐藏程序输出结果

net stop myservices >nul 2>nul

来自 <[https://blog.csdn.net/earbao/article/details/51790405](https://blog.csdn.net/earbao/article/details/51790405)>

### 2.1. 重定向操作符 描述 

\>  将命令输出写入到文件或设备（如打印机），而不是命令提示符窗口或句柄。
<  从文件而不是从键盘或句柄读入命令输入。
\>>  将命令输出添加到文件末尾而不删除文件中已有的信息。
\>& 将一个句柄的输出写入到另一个句柄的输入中。
<&  从一个句柄读取输入并将其写入到另一个句柄输出中。
|  从一个命令中读取输出并将其写入另一个命令的输入中。也称作管道。

来自 <[https://blog.csdn.net/earbao/article/details/51790405](https://blog.csdn.net/earbao/article/details/51790405)>
## 3. cmd 一行命令执行多条指令

aa && bb
means：执行aa，成功后再执行bb
```cmd
node a.js && node b.js
```
如果a.js运行失败则b.js不会再运行

aa || bb
means：先执行aa，若执行成功则不再执行bb，若失败则再执行bb
```cmd
node a.js || node b.js
```
如果a.js运行失败则b.js再运行，如果a.js运行成功则b.js不再运行

aa & bb
means：先执行aa再执行bb，无论aa是否成功
```cmd
node a.js & node b.js
```
先运行a.js运行，不管运行a.js文件是否报错，b.js接着运行

来自 <[https://blog.csdn.net/yrk0556/article/details/104308866](https://blog.csdn.net/yrk0556/article/details/104308866)>