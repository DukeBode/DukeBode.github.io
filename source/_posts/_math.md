---
title: _math
date: 2023-08-07 20:56:45
cover:
tags:

mindmap-plugin: basic
number headings: first-level 2, auto,max 3
---

<!-- more -->

## 1 极限与连续

### 1.1 函数

#### 1.1.1. 函数概念

- $y=f(x),x\in{D}$
- 自变量 $x$
- 因变量 $y$
- 定义域 $D$
- 值域 $R_{f}=f(D)=\{y|y=f(x),x\in{D}\}$

##### 符号函数
- $$y=sgnx=
 \left\{\begin{aligned}
	-1&,x<0\\
 0&,x=0\\
 1&,x>0
 \end{aligned}\right.$$
##### 取整函数
- $x-1<[x]<x$
#### 1.1.2. 复合函数

#### 1.1.3. 反函数
- $y=f(x)$和$x=f^{-1}(y)$的图形重合
- $y=f(x)$和$y=f^{-1}(x)$的图形关于直线$y=x$对称
- $f^{-1}(f(x))=x$
- $f(f^{-1}(x))=x$

#### 初等函数
> 由常数和基本初等函数经过有限次四则运算和有限次的函数复合步骤所构成并可用一个式子表示的函数

##### 基本初等函数
1. 幂函数
	1. $y=x^{\mu},(\mu为实数)$ 

2. 指数函数
	1. $y=a^x,(a>0,a\neq1)$

3. 对数函数
	1. $y=log_{a}x,(a>0,a\neq1)$

4. 三角函数
	1. 正弦函数 $y=\sin(2k\pi+x)=-\sin(x\pm\pi)=-\sin(-x)=\sin(\pm\pi-x)=\mp\cos(x\pm\frac{\pi}{2}),k\in\mathbb{Z}$
	2. 余弦函数 $y=\cos(2k\pi+x)=-cos(x\pm\pi)=\cos(-x)=-\cos(\pm\pi-x)=\pm\sin(x\pm\frac{\pi}{2}),k\in\mathbb{Z}$
	4. 正切函数 $y=\tan(2k\pi+x)=\tan(x\pm\pi)=-\tan(-x)=-\tan(\pm\pi-x)=-tan(x\pm\frac{\pi}{2})=\frac{\sin(2k\pi+x)}{\cos(2k\pi+x)},k\in\mathbb{Z}$
	5. 余切函数 $y=\cot(2k\pi+x)=\cot(x\pm\pi)=-\cot(-x)=-\cot(\pm\pi-x)=\frac{1}{\tan(2k\pi+x)}=\frac{\cos(2k\pi+x)}{\sin(2k\pi+x)},k\in\mathbb{Z}$
	6. 正割函数 $y=\sec(2k\pi+x)=\frac{1}{cos(2k\pi+x)},k\in\mathbb{Z}$
	7. 余割函数 $y=\csc(2k\pi+x)=\frac{1}{\sin(2k\pi+x)},k\in\mathbb{Z}$

5. 反三角函数
	1. $y=\arcsin(x)$
	2. $y=\arccos(x)$
	3. $y=\arctan(x)$
#### 函数的性态
##### 单调性
##### 奇偶性
- 偶函数 $f(-x)=f(x)$
	- $x^2$
	- $\mid x \mid$
	- $cos(x)$
	- $f(x)+f(-x)$
- 奇函数 $f(-x)=-f(x)$
	- $\sin(x)$
	- $\tan(x)$
	- $arcsin(x)$
	- $arctan(x)$
	- $\ln(\frac{1-x}{1+x})$
	- $\ln(x+\sqrt{1+x^2})$
	- $\frac{e^x-1}{e^x+1}$
	- $f(x)-f(-x)$
##### 周期性

有界性
### 1.2 极限
### 1.3 连续
## 2 导数与微分

## 3 一元函数微分学

## 4 不定积分
## 5 定积分
## 6 多元函数微分学
## 7 微分方程
## 8 重积分
## 9 级数
## 10 空间解析几何
## 11 曲线积分与曲面积分
## 12 数学的经济应用

## 13 随机事件和概率
## 14 随机变量及其分布
## 15 多维随机变量及其分布
## 16 随机变量的数字特征
## 17 大数定律和中心极限定理
## 18 数理统计的基本概念
## 19 参数估计
## 20 假设检验

## 21 行列式

### 21.1 概念

排列
逆序
逆序数

上（下）三角形行列式
### 21.2 性质
1. 经过转置行列式的值不变
2. 某行有公因子k，可把k提出
	1. 某行元素全为0，则为0
3. 两行互换，行列式的值变号
	1. 两行相同，则为0
	2. 两行成比例，则为0
4. 如果某行每一项都是两数之和，则可以拆成两个行列式之和，其它行不变
5. 某行k倍加到另外一行，值不变

### 21.3 展开式
$a_{ij}$余子式,$M_{ij}$
$a_{ij}$代数余子式$A_{ij}=(-1)^{i+j}M_{ij}$
按行展开，$\begin{vmatrix}A\end{vmatrix}=\sum\limits_{k=1}^na_{ik}A_{ik},i=1,2,\cdots,n$，按列展开$\begin{vmatrix}A\end{vmatrix}=\sum\limits_{k=1}^{n}a_{kj}A_{kj},j=1,2,\cdots,n$

计算

## 22 矩阵

## 23 n维向量
## 24 线性方程组
## 25 特征值与特征向量
## 26 二次型
