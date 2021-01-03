<!--
 * @Author: your name
 * @Date: 2019-11-09 21:44:03
 * @LastEditTime: 2020-04-26 14:28:12
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \DukeBode.github.io\source\_posts\python-wheel.md
 -->
---
title: python wheel 打包
date: 2019-11-09 21:44:03
cover:
tags:
- python
---

[官方教程](https://packaging.python.org/)
[概述](https://packaging.python.org/overview/)
[教程](https://packaging.python.org/tutorials/)
[指南](https://packaging.python.org/guides/)

<!-- more -->

### github action

1. 创建 GitHub 仓库
1. 配置 pypi token
1. 配置 action 脚本
1. 配置本地 git 环境
1. 配置 本地仓库
1. 配置打包及开发环境

### 最小pypi包

```sh
.gitignore
LICENSE
README.md
setup.py
docs/
    /README.md
module/
    /__init__.py # python 包标志
    /__main__.py
```

### 打包环境

```sh
# bdist
# bdist_wheel
pip install setuptools wheel twine
# twine upload dist/*
```

### __init__.py

> __init__.py 文件表明当前文件夹为 Python 模块,模块被导入时实际为此文件，模块方式运行时先执行此文件。

#### __init__.py 中常配置的模块参数

- __all__ 指定 `form package import *` 的内容
- __version__ 指定版本

### __main__.py

> __main__.py 文件表明当前文件夹可作为模块运行，可以文件夹、模块方式运行时执行此文件，相当于依赖模块的示例程序。

### setup.py

> setup.py 文件是 setuptools 打包的脚本文件，文件内应当写明包相关信息，以及其它的附属操作。

```py
# 官方示例
# https://github.com/pypa/sampleproject/blob/master/setup.py

# read the contents of README file
with open("README.md", "r", encoding='utf-8') as fh:
    long_description = fh.read()

setuptools.setup(
    # https://packaging.python.org/guides/distributing-packages-using-setuptools/
    name="example-pkg-YOUR-USERNAME-HERE", # Replace with your own username
    version="0.0.1",
    author="Example Author",
    author_email="author@example.com",
    description="A small example package",
    long_description=long_description,
    long_description_content_type="text/markdown",
    url="https://github.com/pypa/sampleproject",
    packages=setuptools.find_packages(),
    classifiers=[
        # https://pypi.org/classifiers/
        "Programming Language :: Python :: 3",
        "License :: OSI Approved :: MIT License",
        "Operating System :: OS Independent",
    ],
    python_requires='>=3.6',
)
```
