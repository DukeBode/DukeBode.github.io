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

## 1. 参考文档
1. [Installing the Jupyter Software](https://jupyter.org/install)
1. [Jupyter kernels](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels)

https://github.com/conda-forge/miniforge

## 2. kernel

### 2.1. IJulia

```julia
add IJulia
using IJulia
notebook()
```

https://github.com/JuliaLang/IJulia.jl

### 2.2. C

```sh
pip install jupyter-cpp-kernel
```

https://github.com/shiroinekotfs/jupyter-cpp-kernel

### 2.3. IR
```R
install.packages('IRkernel')
IRkernel::installspec(user = FALSE)
jupyter labextension install @techrah/text-shortcuts
```

### 2.4. dot-kernel

```sh
pip install dot_kernel
install-dot-kernel
```

https://github.com/laixintao/jupyter-dot-kernel

### 2.5. octave

```sh
pip install octave-kernel
```

https://github.com/calysto/octave_kernel

### 2.6. kotlin-jupyter

```sh
pip install kotlin-jupyter-kernel
```

https://github.com/Kotlin/kotlin-

### 2.7. java

```sh
java -jar ganymede-2.1.2.20230910.jar -i
```

https://github.com/allen-ball/ganymede

### 2.8. other

https://github.com/jupyter/jupyter/wiki/Jupyter-kernels

## 3. 设置默认起始目录

1. 使用 shell 打开配置文件

```sh
# 获取默认配置文件路径，有配置的同学请按 N。
jupyter notebook --generate-config
# vim 编辑配置文件，Windows下没有也可以用 start。
vim ~/.jupyter/jupyter_notebook_config.py
```
2. 取消`c.NotebookApp.notebook_dir`注释，即删除行前`#`符号
3. 将要设置的默认起始目录填入后面的引号之中。