---
title: python 组合数
date: 2020-01-05 13:28:31
cover:
tags:
TeX: true
---

组合是数学的重要概念之一。从 n 个不同元素中每次取出 m 个不同元素 ，不管其顺序合成一组，称为从 n 个元素中不重复地选取 m 个元素的一个组合。所有这样的组合的种数称为组合数。

<!-- more -->
$$ C_n^m=\frac{A_n^m}{m!}=\frac{n!}{(n-m)!m!}=\frac{\prod_{i=n-m+1}^{n}i}{m!}=C_n^{n-m} \quad (n \geq m \geq 1)$$

结论：
1. 从n个不同元素中取出m个元素的组合数即n的阶乘除以除以(n-m)的阶乘与m的阶乘的积的商。

```py
from math import factorial
def combinations(n,m):
    return factorial(n)//factorial(m)//factorial(n-m)
```

1. 化简可得，从n个不同元素中取出m个元素的组合数即出现一次的偏大整数的积除以出现三次的偏小整数的积的商。

```py
def combinations(n,m):
    result = 1
    min,max=sorted((m,n-m))
    for i in range(n,0,-1):
        if i>max:
            result *= i
        elif i <= min:
            result = result // i
    return result
```

1. n个连续整数的积可被n的阶乘整除。

```py
def combinations(n,m):
    result = 1
    for i in range(m):
        result=result*(n-i)//(i+1)
    return result
```

1. 从n个不同元素中取出m个元素的组合数与从n个不同元素中取出(n-m)个元素的组合数相等。

```py
def combinations(n,m):
    result = 1
    for i in range(min(n-m,m)):
        result=result*(n-i)//(i+1)
    return result
```

[Python版组合数计算方法优化思路和源码](https://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ==&mid=2247484700&idx=1&sn=a92cd5b572f3426215c5077edd911566&chksm=eb8aae46dcfd27504c6c32c3c2b7d12756b97b2850354366e7841ca71df38e9590891dea9c5f&mpshare=1&scene=1&srcid=0105CnjEy8AVCvacDDGmaD2l&sharer_sharetime=1578196700974&sharer_shareid=3726fbb92179608ce6915a88bf3209c9&exportkey=AeVJmUCXvaPlGzrSnNstWZE%3D&pass_ticket=BTWnZASExfQ2s44l%2Faa1gGcF8st07sk22Ohh%2BQylaMjuas6mCV6xn8HzMRrOrhta#rd)