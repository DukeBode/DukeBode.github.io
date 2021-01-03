---
title: Cascading Style Sheets
date: 2020-01-21 21:41:54
cover:
tags:
  - 前端
---

Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

<!-- more -->

引入层叠样式表的方法包括：
外联式样式表
例：

```html
<head>
  <link rel="stylesheet" href="/css/default.css">
</head>
```

属性：rel 用来说明<link>元素在这里要完成的任务是连接一个独立的css文件。而href属性给出了所要连接css文件的url地址

内嵌式样式表：
例：
```html
<head>
  <style type="text/css">
    td{
      font:9pt;
      color:red
      }
    .font105{
      font:10.5pt;
      color:blue
      }
  </style>
</head>
```
元素内定
格式：`<p style="font-size:10.5pt">`
导入式样式表
```html
〈html>
<head>
<style type="text/css">
<!--
@import url(css/home.css);
-->
<body>
....
</body>
</html>
```

css的优先级
越接近目标的样式定义优先级越高，高优先级样式将继承低优先级样式的未重叠定义但覆盖重叠的定义
如果4种样式表对同一元素定义了不同的样式，那么他们的优先级顺序从高到低是，元素内定，内嵌样式表，导入样式表，外联样式表。
css结构
例：td{font-size:10.5pt;color:#666666}
css样式包含两个基础部分，
选择符<td>和声明{font-size:10.5pt;color:#666666}
声明也有两部分组成：
属性font-size,color和值10.5pt,#666666
选择符分为6种
1元素选择符
当页面上多个元素的样式相同时，可以将多个元素放在一起定义，中间以逗号分开 例：
```css
td,p,li,input,select{font-size:12px;}
```

2class(类)选择符
例：
```html
<head>
<title>.....</title>
<style type="text/css">
<!--
.red{font-size:10.5pt;color:#ff0000}
-->
</head>
<body bgcolor="#ffffff">
<p class="red">士大夫井冈山地方官
</body>
```
还有一种方法就是限定可以应用它的页面元素
例：
```html
<head>
<title>.....</title>
<style type="text/css">
<!--
h1.red{color:#ff0000}
-->
</head>
<body bgcolor="#ffffff">
<p class="red">士大夫井冈山地方官

<h1 class="red">九连环离开计划</h1>
</body>
```
3 id选择符
与class选择附类似，只是把'.'换成'#'
例：

```html
<html>
<body>
<head>
<style type="text/css">
#select{font-size:18px;color:#0000ff}
</style>
</head>
<body>
<table width="250" border="1" height="50">
<tr>
<td align="center" id="select">id选择符</td>
</tr>
</table>
</body>
</html>
```

我们看到在调用ID选择附时与CLASS选择附类似，只是将class=""换成了id=""，方便页面脚本语言的调用
关联选择符

```html
<html>
<body>
<head>
<style type="text/css">
<!--
td p{font-size:18px;color:#0000ff}
-->
</head>
<body>
<table width="250" border="1" height="50">
<tr>
<td align="center">
关联选择符
</td>
</tr>
</table>
关联选择符
</body>
</html>
```
我们设定了在元素中<td>的元素所包含文字的样式，只有在两个条件都满足是，样式在会起作用，

伪类选择符
是只能用在css选择符里，而不能用在html代码中的选择符
例：

```html
<html>
<head>
<style type="text/css">
a:link{color:#000000}
a:visited{color:#cccccc}
a:hover{color:#ff0000}
a:active{color:#ooooff}
</style>
</head>
<body>
<a href="#">关联选择符</a>
<a href="#">关联选择符</a>
<a href="#">关联选择符</a>
<a href="#">关联选择符</a>
〈/body>
</html>
```

正确的顺序是a:link\a:visited\a:hover否则会引起页面上连接颜色混乱

伪元素选择符
与伪类选择符定义类似，目前被大多数浏览器支持的有两个：首行伪元素（first-line）和首字符伪元素(first-letter)是用来实现首行大写和首行下沉效果的
例：首行

```html
<html>
<head>
<!--
p:first-line{color:red;font-size:20pt}
-->
</head>
<body>
dfgsadfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdf...
</body>
</html>
```

长度随浏览器窗口大小而改变
首字

```html
<html>
<head>
<!--
p:first-letter{color:red;font-size:50pt;float:left;}
-->
</head>
<body>
dfgsadfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdfgsdf...
</body>
</html>
```

以上两种都只能应用于块状元素上

css规则
1.继承

```html
<html>
<head>
<style type="text/css">
<!--
td{font-size:12pt}
p{color:red}
-->
</hesd>
<body>
<table width="300" border="1" height="150">
<tr>
<td align="center">css规则</td>
</table>
</body>
</html>
```

为最高级<td>次一级两种css用在一个属性元素上，相同的覆盖，不同的继承，

2.组合

```css
td{font-size:12pt}
.p1{font-size:12pt}
```

组合后

```css
td,.p1{font-size:12pt}
```

3.层叠
在样式里定义过后，在表格属性中又定义一次
```html
<html>
<head>
<style type="text/css">
<!--
red{color:#ff0000 limportant}
-->
</hesd>
<body>
<table width="300" border="1" height="150"><tr>
<td align="center" style="color:#0000ff" class="red">决撒地方官</td>
</tr>
</table>
</body>
</html>
```

- css单位
分四大类：
1. 长度单位
数值可以是整数，小数，正数，负数，0，后加单位（负值不要轻易使用）
换算关系：
1in(英寸)=6pc(派)
1in(英寸)=72pt(磅)
1in(英寸)=2.54(厘米)
1cm(厘米)=10mm(毫米)
1cm(厘米)=0.3937(英寸)
1pt(磅)=1/72in(英寸)=0.2478mm(毫米)
1pc(派)=1/6in(英寸)=我国新四号铅字的尺寸
1. 百分比单位
1. 颜色单位
1. url单位
```css

div属性
color : #999999   文字颜色
font-family : 宋体 文字字型
font-size : 10pt 文字大小
font-style:itelic 文字斜体育
font-variant:small-caps 小字体
letter-spacing : 1pt 文字间距
line-height : 200% 设定行高
font-weight:bold 文字粗体
vertical-align:sub 下标字
vertical-align:super 上标字
text-decoration:line-through 加?h除线
text-decoration:overline 加顶线
text-decoration:underline 加底线
text-decoration:none ?h除连接底线
text-transform : capitalize 首字大写
text-transform : uppercase 英文大写
text-transform : lowercase 英文写
text-align:right 文字*右对齐
text-align:left 文字*左对齐
text-align:center 文字置中对齐
这些是一些简单的文字效果，可以应用到css的页面中。　
背景
background-color:black 背景颜色
background-image : none 背景图片
background-attachment : fixed 固定背景
background-repeat : repeat 重复排列-网页预设
background-repeat : no-repeat 不重复排列
background-repeat : repeat-x 在x轴重复排列
background-repeat : repeat-y 在y轴重复排列
background-position : 90% 90% 背景图片x与y轴的位置 　
链接
A 所有超连接
A:link 超连接文字格式
A:visited 浏览过的连接文字格式
A:active 按下连接的格式
A:hover 鼠标移至连接
边框
border-top : 1px solid black 上框
border-bottom : 1px solid #6699cc 下框
border-left : 1px solid #6699cc 左框
border-right : 1px solid #6699cc 右框
border: 1px solid #6699cc 四边框
```