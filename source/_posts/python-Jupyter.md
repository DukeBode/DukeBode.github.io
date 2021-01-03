---
title: Jupyter
date: 2019-07-16 17:57:16
cover:
tags: 
- 编辑器
- IDE
---

<!-- more -->

```sh
# 安装
pip install jupyterlab

```

## 参考文档
1. [Installing the Jupyter Software](https://jupyter.org/install)
1. [Jupyter kernels](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels)


## 配置内核

## 设置默认起始目录

1. 使用 shell 打开配置文件

```sh
# 获取默认配置文件路径，有配置的同学请按 N。
jupyter notebook --generate-config
# vim 编辑配置文件，Windows下没有也可以用 start。
vim ~/.jupyter/jupyter_notebook_config.py
```
2. 取消`c.NotebookApp.notebook_dir`注释，即删除行前`#`符号
3. 将要设置的默认起始目录填入后面的引号之中。