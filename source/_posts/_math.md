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
- \$$y=sgnx=\left\{\begin{aligned}-1&,x<0\\0&,x=0\\1&,x>0\end{aligned}\right.$$
##### 取整函数
- \$$x-1<[x]<x$$
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
$$
\begin{align}
&导数公式&&积分公式\\
&(C)'=0 &&\int 0dx=C\\
&\begin{split}
&(x^a)'=a x^{a-1}\\
&(\ln{\left|x\right|})'=\frac{1}{x}\\
&(\log_a{x})'=\frac{1}{x\ln{a}}\end{split} && \int x^adx=
\begin{cases}\frac{1}{a+1}x^{a+1}+C &,a\neq-1\\
\ln{\left|x\right|}+C&,a=-1
\end{cases}\\
&(a^x)'=a^x\ln a &&\int a^xdx=\frac{a^x}{\ln a}+C,(a>0,a\neq1)\\
&(e^x)'=e^x&&\int e^xdx=e^x+C \\
&(\sin{x})'=\cos{x}&&\int \sin xdx=-\cos x+C\\
&(\cos{x})'=-\sin{x}&&\int\cos xdx=\sin x+C\\
&(\tan{x})'=\sec^2{x}&&\int\sec^2 xdx=\tan x+C\\
&(\cot{x})'=-\csc^2{x}&&\int\csc^2 xdx=-\cot x+C\\
&(\sec{x})'=\sec{x}\tan{x}
&&\begin{split}&\int\sec x\tan xdx=\sec x+C
\\&\int\sec xdx=\ln\left|\sec x+\tan x\right|+C\end{split}\\
&(\csc{x})'=-\csc{x}\cot{x}
&&\begin{split}&\int\csc x\cot xdx=\csc x+C
\\&\int\csc xdx=-\ln\left|\csc x+\cot x\right|+C\end{split}\\
&(\arcsin{x})'=\frac{1}{1-x^2}
&&\int\frac{1}{\sqrt{a^2-x^2}}dx=\arcsin\frac{x}{a}+C\\
&(\arccos{x})'=-\frac{1}{\sqrt{1-x^2}}\\
&(\arctan{x})'=\frac{1}{1+x^2}
&&\begin{split}
&\int\frac{1}{a^2+x^2}dx=\frac{1}{a}\arctan\frac{x}{a}+C\\
&\int\frac{1}{x^2-a^2}dx=\frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right|+C\end{split}\\
&(\arccot{x})'=-\frac{1}{1+x^2}\\
& 
&&\begin{split}&\int\frac{1}{\sqrt{x^2+a^2}}dx=\ln(x+\sqrt{x^2+a^2})+C\\
&\int\frac{1}{\sqrt{x^2-a^2}}dx=\ln\left|x+\sqrt{x^2-a^2})\right|+C
\end{split}
\end{align}
$$
高阶导数公式
$$
\begin{align}
&\left(\sin{x}\right)^{\left(n\right)}=\sin\left(x+n\cdot\frac{\pi}{2}\right)\\
&(\cos{x})^{(n)}=\cos\left(x+n\cdot\frac{\pi}{2}\right)\\
&(u\pm{v})^{(n)}=u^{(n)}\pm{v^{(n)}}\\
&(uv)^{(n)}=\sum_{k=0}^{n}C_n^ku^{(k)}v^{(n-k)}
\end{align}
$$
泰勒公式
拉格朗日余项
$$\begin{align}
&f(x)=\left(\sum_{n=0}^\infty\frac{1}{n!}f(x_0)^{(n)}(x-x_0)^n\right)+o[(x-x_0)^n] \\
&f(x)=\left(\sum_{n=0}^\infty\frac{1}{n!}f(0)^{(n)}x^n\right)+o(x^n)\\
&f(x)=\left(\sum_{n=0}^\infty\frac{1}{n!}f(x_0)^{(n)}(x-x_0)^n\right)+\frac{f(\xi)^{(n+1)}}{(n+1)!}(x-x_0)^{n+1} \\
&e^x=\left(\sum_{n=0}^\infty\frac{x^n}{n!}\right)+\frac{e^{\theta x}}{(n+1)!}x^{n+1},\theta\in(0,1)\\
&\sin x=\left(\sum_{n=1}^\infty(-1)^{n-1}\frac{x^{2n-1}}{(2n-1)!}\right)+(-1)^n\frac{\cos(\theta x)}{(2n+1)!}x^{2n+1},\theta\in(0,1)\\
&\cos x=\left(\sum_{n=0}^\infty(-1)^n\frac{x^{2n}}{(2n)!}\right)+(-1)^{n+1}\frac{\cos(\theta x)}{(2n+2)!}x^{2n+2},\theta\in(0,1)\\
&\ln{(1+x)}=\left(\sum_{n=1}^\infty(-1)^{n-1}\frac{x^n}{n}\right)+(-1)^n\frac{x^{(n+1)}}{(n+1)(1+\theta x)^{n+1}},\theta\in(0,1)\\
&(1+x)^a=\left(\sum_{n=0}^\infty\tbinom{a}{n}x^n\right)+\tbinom{a}{n+1}(1+\theta x)^{a-n-1}x^{n+1},\theta\in(0,1)
\end{align}$$
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
