---
title: iPad
date: 2023-04-28 22:17:47
tags: 
  - iPad 
  - iPadOS
---

iPad 的一些问题，软件。
Your next computer is not a computer.

<!-- more -->

## 1. 开关机
### 1.1. 将 iPad 开机：
- 按住锁屏按钮，直到出现 Apple 标志。
### 1.2. 将 iPad 关机：
- 同时按住锁屏按钮及任一音量按钮，然后拖移滑块。
### 1.3. 强制重新启动 iPad

1. 按住离顶部按钮最近的音量按钮，然后快速松开。
2. 按住离顶部按钮最远的音量按钮，然后快速松开。
3. 按住顶部按钮，当 Apple 标志出现时，松开顶部按钮

修改锁屏密码应验证账户密码
重置系统自动云备份

## 2. 快捷键

### 2.1. 文稿快捷键

- **Control-A**：移至行或段落的开头。
- **Control-E**：移至行或段落的末尾。
- **Control-F**：向前移动一个字符。
- **Control-B**：向后移动一个字符。
- **Control-H**：删除插入点左边的字符。也可以使用 Delete 键。
- **Control-D**：删除插入点右边的字符。也可以使用 Fn-Delete。
- **Control-L**：将光标或所选内容置于可见区域中央。
- **Control-P**：上移一行。
- **Control-N**：下移一行。
- **Control-O**：在插入点后新插入一行。
- **Control-T**：将插入点后面的字符与插入点前面的字符交换。
- **Control-K**：删除插入点与行或段落末尾处之间的文本。
- **Command-左花括号 ({)**：左对齐。
- **Command-右花括号 (})**：右对齐。
- **Shift-Command-竖线 (|)**：居中对齐。

https://support.apple.com/zh-cn/HT201236

## 3. 应用

- [a-Shell](https://apps.apple.com/cn/app/a-shell/id1473805438)
- [Swift Playgrounds](https://apps.apple.com/cn/app/swift-playgrounds/id908519492)
- [LocalSend](https://apps.apple.com/cn/app/localsend/id1661733229)
- [vimlike](https://apps.apple.com/cn/app/vimlike/id1584519802)
- [spacedesk](https://apps.apple.com/cn/app/spacedesk-multi-monitor-app/id1069217220)
- [obsidian](https://apps.apple.com/cn/app/obsidian-connected-notes/id1557175442)
- 
### 3.1. [KeKa - 压缩文件管理器](https://apps.apple.com/cn/app/keka-%E5%8E%8B%E7%BC%A9%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8/id6443677513)

### 3.2. [ish](https://apps.apple.com/cn/app/ish-shell/id1436902243)
#### 3.2.1. Alpline Linux

#### 3.2.2. 查看版本

```sh
cat /etc/os-release
cat /etc/alpine-release
```

#### 3.2.3. 配置源
```sh
sed -i 's#http://apk.ish.app/v3.19-2024-08-01#https://mirrors.tuna.tsinghua.edu.cn/alpine/v3.19#g' /etc/apk/repositories
# 
cat /etc/apk/repositories
# 更新包列表
apk update
# 
apk upgrade
# 
apk add git openssh cmake vimdiff
apk add crago
apk add python3 python-pip
apk add gcompat
```
#### 3.2.4. git 配置

##### 3.2.4.1. config 文件配置

```config
# github
# https://github.com/
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~\.ssh\github
```

```sh
apk add git openssh
# 查看 git 版本
git version
# 设置 git 全局用户名
git config --global user.name "DukeBode"
# 设置 git 全局邮箱
git config --global user.email 29868250+DukeBode@users.noreply.github.com
# 格式 
# ssh-keygen -t rsa -C "通常为邮箱" -f "私钥文件绝对路径"
ssh-keygen -t ed25519 -C "giee.com" -f "~/.ssh/gitee"
ssh-keygen -t ed25519 -C "github.com" -f "~/.ssh/github"
ssh-keygen -t ed25519 -C "gitlab.com" -f "~/.ssh/gitlab"
ssh-keygen -t ed25519 -C "gitcode.com" -f "~/.ssh/gitcode"
ssh -T git@github.com
```

##### 3.2.4.2. 中文字符路径问题

```sh
git config --global core.quotepath false 
git config --global i18n.logOutputEncoding utf-8 
git config --global i18n.commitEncoding utf-8
```

#### 3.2.5. 异常处理

fatal error: stdio.h: No such file or directory
```sh
apk add musl-dev
```

clang: error: unable to execute command: Executable "ld" doesn't exist!
```sh
apk add binutils
```

#### 3.2.6. 挂载

```sh
mkdir -p ~/obsidian
# 在弹出的文件夹中选择你要挂载的目录
mount -t ios . obsidian
```

https://wiki.alpinelinux.org/wiki/Running_glibc_programs
https://github.com/sgerrand/alpine-pkg-glibc

## 4. 设置-通用-键盘

- 关闭智能标点 2023-11-12
- 关闭首字母自动大写 2023-11-12
- 关闭句号快捷键 2023-11-12 

## 5. 已知问题

-  使用外接显示器时Ipad必须常亮 2023-11-12
- 外接显示器触屏不可操作 2023-11-12
- 多个视频、音乐无法同时播放 2023-11-12
- APP资源库使用起来非常低效 2023-11-12
- 不可以设立空的主屏幕 2023-11-12
- 连接外接显示器，无键鼠不可操作 2023-11-12
- 第三方App 无法使用Apple pencil 进行App外截图 2023-11-12
- 第三方输入法不支持键盘 2023-11-12
- 缺乏系统级返回按钮/手势，需应用适配 2023-11-12
- 【cmd W】退出快捷键部分软件不支持 2023-11-12
- 文件管理方式复杂，冗余存储严重，不同于缓存处理，有时可以直接编辑，有时需要副本编辑。
- 复制粘贴麻烦，软件自动捕获剪切板提示严重，不如鸿蒙系统的暂存区好用直观。
- 分辨率无法调整，屏幕大但显示依然小，放大镜的作用不大。
- 文件备份严重依赖iCloud存储，很多软件只支持iCloud丢文件，无法本地查看，无法使用其它方式备份。
- 通知管控极其麻烦，需要逐个手动处理，很是麻烦，默认开启。
- 桌面花里胡哨，应用图标一堆，找起来非常麻烦，尤其记不得名字叫啥的软件，缺乏手势快捷启动。
- 充电速度低下，虽然支持30W的充电，但送的充电头只有20W。
- 官方服务只支持苹果设备，对非苹果设备兼容性非常差。

## 6. 外接显示器

- 外接显示器的触摸功能与键鼠操作存在冲突，触摸后键鼠失灵
- 播放视频时暂停不方便，平板上也无遥控器功能
- 视频软件兼容性差，部分全屏难
- 发热挺严重
