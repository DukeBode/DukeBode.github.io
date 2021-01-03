---
title: Windows
date: 2020-03-24 13:55:33
cover:
tags:
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


备份

- 环境变量 set path
- 配置文件 wifi、ssh、gradle
```sh
# 显示配置文件
netsh wlan show profile

# 导出 WiFi 文件
netsh wlan export profile folder=D:\ key=clear
```
- 软件安装包

