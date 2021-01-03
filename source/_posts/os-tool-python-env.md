---
title: Python 3.x
date: 2018-11-17 21:29:32
tags: 
- python
- Django
- 框架
---

## Python 3 安装

<!-- more -->

## pypi 源配置

### 常见在线 pypi repository
- 华为云 https://mirrors.huaweicloud.com/repository/pypi/simple
- 清华 https://pypi.tuna.tsinghua.edu.cn/simple

### 配置 pypi 镜像源

```sh
# 更新 pip 至最新版
pip install -i <pypi repository> pip -U
# 配置 pypi 镜像源
pip config set global.index-url <pypi repository>
```

## Pip 包管理

[官网](https://pip.pypa.io)

```sh

# 导出依赖包名至 requirements.txt
pip freeze > requirements.txt
# 安装 requirements.txt 中列出的包
pip install -r requirements.txt
# 卸载包
pip uninstall [options] <package>
# 卸载 requirements.txt 中列出的包
pip uninstall [options] -r <requirements file>
# Options:
# -r, --requirement <file>
# -y, --yes  不询问，直接卸载
```

## conda 包管理

- [conda 官网](https://docs.conda.io/en/latest/)
https://docs.conda.io/en/latest/miniconda.html

## 
- [官网](https://www.python.org/) 
- [文档](https://docs.python.org) 
- [包管理工具 pip](https://pip.pypa.io/)

## 切片

```python
List[start:end:step]
# 反转列表
List[::-1]
```