---
title: shell
date: 2018-08-22 11:58:48
cover:
tags:
---

<!-- more -->

## 重定向

在 shell 中输入命令运行程序，程序的正常输出信息（标准输出）和一些出错信息（标准错误）会通过 shell 显示在屏幕上。

有时候我们并不需要把这些输出信息（包括标准输出和标准错误）显示在屏幕上，或需要把这些输出信息保存在一个文件中，这时就需要进行输出重定向。输入重定向也是如此。

执行重定向操作的是 shell ，而不是程序。 shell 把重定向符号解释成指令，将标准输出（或标准错误）指向文件，而不是当前显示设备。输入重定向也是如此。

shell将<、>、>>解释成指令，用来把一条命令的输入或输出重定向到一个文件。


类型 | 操作符 | 用途
-|-|-
重定向标准输入 | < | 将命令中接收输入的途径由默认的键盘更改为指定的文件
重定向标准输出 | > | 以替换的方式将命令的执行结果输出到指定的文件，而不是直接显示在屏幕上 
- | >> | 将命令执行的结果追加输出到指定文件
重定向标准错误 | 2> | 清空指定文件的内容，并将标准错误信息保存到该文件中
- | 2>> | 将标准错误信息追加输出到指定的文件中
重定向标准输出和标准错误 | &>或>& | 将标准输出、标准错误的内容全部保存到指定的文件中，而不是直接显示在屏幕上

## 管道

shell在解释命令遇到 | 时会创建管道，并创建两个进程，把标准输入输出重
定向到管道，前一个进程向管道写数据，后一个进程从管道读数据。

查找名称含有gcc的文件并使用wc计数
sudo find / -name gcc | wc –l

查找名称含有ssh的进程
ps -ef | grep ssh

分页查看内容
ls –l –R /usr/share | less

排序文件
ls | sort –r

## 脚本

## bash快捷键

|按键|含义|
---:|:-----|
^A | 光标移到行首
^B | 光标非破坏退格
^C | 中断前台程序
^D | 退出shell
^E | 光标移到行尾
^F | 光标右移
^G | 
^H | 
^I | 
^J | 新行
^K | 删除光标后所有字符
^L | 清屏
^U | 删除光标前所有字符
^R | 搜索历史命令，利用关键字
ALT+. | 引用上一个命令的最后一个参数
ESC+. | 引用上一个命令的最后一个参数
!$ | 引用上一个命令的最后一个参数