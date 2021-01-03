---
title: Python Windows
date: 2019-10-21 20:52:43
cover:
tags:
- python
---

<!-- more -->

### Window 下 Python 多版本问题

- python 2 使用 python
- python 3 使用 py
- python x.y 使用 py -x.y

### 项目虚拟运行环境

```sh
# 指定 python 版本 x.y 创建虚拟环境
py -x.y -m venv env
# 激活环境
.\env\Scripts\activate
# 更新 pip
python -m pip install --upgrade pip
# 退出环境
deactivate
```

### 搭建本地 pypi 服务器

[pypi-server](https://pypi.org/project/pypiserver/)

- 服务器端

```sh
# 安装 pypiserver
pip install pypiserver [passlib，watchdog]
# 创建包目录
mkdir packages
# 启动 pypiserver
pypi-server -p 8080 --fallback-url https://pypi.tuna.tsinghua.edu.cn/simple -d packages packages
```

- 客户端

```sh
pip config set global.index-url http://localhost:8080/simple
```


## python 内存

### 变量 id() 相等，即 a is b

- 整数范围在[-5,256]的变量，即小整数
- 没有空格等特殊字符的字符串，应用 账号

### gc（garbage collection）垃圾回收机制

- 引用计数机制 
    sys.getrefcount(obj) 获取引用计数
    增加引用计数
        对象赋值
        对象作为形参
        对象计入到列表
    减少引用计数
        从列表删除
        del obj
- gc.disable() 关闭垃圾回收机制，测试使用，开发不要用
gc.get_threshold() 获取gc模块中自动执行垃圾回收的频率
gc.get_count() 获取当店自动执行垃圾回收的计算器
gc.set_threshold() 设置自动执行垃圾回收的频率
gc.collect() 手动调用
- 隔代回收机制
    相互引用。。。

### 内置属性

__dict__ 类属性 由类属性构成的字典
__doc__ 类文档
__name__ 类名
__module__ 类所在模块
__bases__  类的父类构成元素，由所有父类组成的元组
__getattribute__ 属性拦截器

### 内建函数

range(start=0,end,step=1)
map(function,iterable)迭代器处理可迭代对象
filter(function,iterable) function 返回true保留
functools.reduce(function,iterable)累function处理
sorted() reverse为ture 则从大到小，自定义对象需要指定key=lambda obj:obj.属性
lambda x:x*2