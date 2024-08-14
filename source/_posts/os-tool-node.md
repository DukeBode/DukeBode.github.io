---
title: Nodejs
date: 2019-08-06 14:16:18
cover:
tags:
- node
- yarn
- npm
---

<!-- more -->

- [清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/)
- [网易开源镜像站](http://mirrors.163.com/)
- [腾讯云软件源站](https://mirrors.cloud.tencent.com/)
- [华为开源镜像站](https://mirrors.huaweicloud.com/)
- [阿里巴巴开源镜像站](https://mirrors.aliyun.com)
- [中国科学技术大学开源软件镜像](http://mirrors.ustc.edu.cn/)
- [东软信息学院开源镜像站](http://mirrors.neusoft.edu.cn/)
- [北京交通大学自由与开源软件镜像站](https://mirror.bjtu.edu.cn/)
- [浙江大学开源镜像站](http://mirrors.zju.edu.cn/)

[官网](https://nodejs.org/)

[nvm](https://github.com/nvm-sh/nvm#node-version-manager---)

[nodesource](https://github.com/nodesource/distributions#enterprise-linux-based-distributions)

## 1. 切换 npm 源

Node 的官方模块仓库网速太慢，模块仓库需要切换到阿里的源。

不安装 cnpm 只用[淘宝镜像](https://npm.taobao.org/)，设置 npm 的镜像：

```sh
npm config set registry https://registry.npm.taobao.org/
```

执行下面的命令，确认是否切换成功。

```sh
npm config get registry
```

## 2. yarn

[官网](https://yarnpkg.com)

https://mirrors.huaweicloud.com/yarn/v1.19.1/yarn-1.19.1.msi
https://mirrors.huaweicloud.com/yarn/

```sh
# 若经常网络异常，执行此句
yarn config set registry https://registry.npm.taobao.org/ -g
yarn config set registry https://mirrors.huaweicloud.com/repository/npm/
```

[如何在CentOS Linux 7.5上安装Node.js](https://www.linuxidc.com/Linux/2018-05/152389.htm)

## 3. java

[Java SE Downloads](https://www.oracle.com/java/technologies/javase-downloads.html)
[Java Documentation](https://docs.oracle.com/en/java/)
[Jakarta® EE Software](https://jakarta.ee/)

yum install java-latest-openjdk

java 中文显示不正常
> JAVA_TOOL_OPTIONS -Dfile.encoding=UTF-8

jlink 部署

## 4. pypi 源配置

### 4.1. 常见在线 pypi repository
- 华为云 https://mirrors.huaweicloud.com/repository/pypi/simple
- 清华 https://pypi.tuna.tsinghua.edu.cn/simple

### 4.2. 配置 pypi 镜像源

```sh
# 更新 pip 至最新版
pip install -i <pypi repository> pip -U
# 配置 pypi 镜像源
pip config set global.index-url <pypi repository>
```

## 5. Pip 包管理

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

## 6. conda 包管理

- [conda 官网](https://docs.conda.io/en/latest/)
https://docs.conda.io/en/latest/miniconda.html

## 7. python
- [官网](https://www.python.org/) 
- [文档](https://docs.python.org) 
- [包管理工具 pip](https://pip.pypa.io/)

### 7.1. 切片

```python
List[start:end:step]
# 反转列表
List[::-1]
```