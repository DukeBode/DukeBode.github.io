---
title: Hyper Text Markup Language
date: 2020-01-21 21:41:54
cover:
tags:
  - 前端
---

HTML (HyperText Markup Language) is the most basic building block of the Web. It defines the meaning and structure of web content.

<!-- more -->

预格式化：

`<pre>......</pre>` 

浏览是效果和编写是效果格式一样

列表

1无序列表又称符号列表

语法格式：

```html
<ul type="">type的属性可选直disc实心圆点,clrcle空心圆点,square实心方框
<li>文字</li>
<li>文字</li>
</ul>
```
2有序列表

语法格式：

```html
<ol type="?" start"?">
<li>文字</li>
<li>文字</li>
</ol>
```

- type的值是编号字符可选的有1...,a...,A...,i... ,I...
- start为起始值例：如果start为3是那么将从3开始，而且必须是数字。

3定义列表
`<dl>`定义列表标记
`<dt>`标示定义条目
`<dd>`标示定义内容
语法格式：

```html
<dl>
<dt>文字</dt>
<dd>文字内容</dd>
</dl>
```

连接和图像
语法格式：
```html
<a href="url" name="?" target="?" title="?">....</a>
```
属性：href 连接目标 值可以是url地址也可以是连接锚点
`<a href="url">...</a>`或者
`<a href="锚点">...</a>`

name 连接名称
语法格式：`<a name="锚点名称">...</a>`
例：
`<a name="abcdcf">...</a>`
连接到该锚点的连接则应是：
`<a name="#abcdef">....</a>`
target目标窗口语法格式：

```html
<a href="url"target="_blank|_self|_farent|_top|windowname">....</a>
```

- -blank打开新窗口
- _self当前窗口打开
一下两个仅在框架叶面中应用
- _parent当前窗口的父级窗口（上一级）打开
- _top在最高一级的窗口打开
- windowname已命名的窗口或框架中打开连接
title连接提示

```html
<a href="http://www.jcwcn.com" title="打开中国教程网的首页">中国教程网</a>
```

图像`<img>`
语法格式：
`<img src="url" alt="?" width="?" height="?" border="?" align="?">`
- border属性定义图片边框的宽度，默认值为0
- align属性设置图片旁边文字的位置

语法格式：`<img src="" align"">`
可选值有：

- top图片和文字顶部对齐
- middle图片和文字居中对齐
- bottom图片和文字底边对齐（默认）
- left图片居左对齐，文字沿图片绕排
- right图片居右对齐，文字沿图片绕排
- absmiddle图片对齐到目前文字行绝对中央
- absbottom图片对齐到目前文字行绝对底部
文字的排版
不换行空白标记

font元素
语法格式：
`<font face="字体名称" size="字体大小" color="字体颜色">`
字体大小可选值为1——7，默认为3
例：`<font face="黑体" size="4" color="#ff00ff">....</font>`

水平线`<hr>`
语法格式：
```html
<hr width="宽度" align="对齐方式默认居中center" size="水平线厚度默认为2" color="颜色" noshade>
```

noshade无阴影，既实线层<div><span>两种元素<div>是块级元素，和段落元素相似，不同的是两个<div>元素之间不会产生两个元素之间的空行，`<span>`是行内元素，可以定义段落中部分文字的属性
语法格式：
`<div align="" style="">...</div>`
align设置层中元素的水平对齐方式
stule设置元素应用css规范的属性
`<div>兼容性比<span>要好一点，最好使用<div>`
表格语法格式：

```html
<table width="" bgcolor="" background="" border="" cellspacing="" cellpadding="">
<tr>...<td>....</td>....</tr>
</table>
```

- border边框宽度默认值为0，既没有边框
- cellspacing表格中单元格的边距大小，默认值为两个像素
- cellpadding表格中单元格之间的间距大小，默认值为两个像素

tr元素
语法格式：
```html
<tr align="" bgcolor="">....</tr>
```
align属性对齐方式可选值如下：left,center,tight,默认为left
bgcolor指定该行的背景颜色
td元素
语法格式：
```html
<td width="宽度" height="高度" align="水平对齐方式" valign="垂直对齐方式" bgcolor="" background="" rowspan="单元格的行跨度" colapan="单元格的列跨度">.....</td>
```
align属性的可选值有：left,center,right
valign属性的可选值有：top,middle,bottom
rowspan和colapan跨行和跨列的数量，默认为1

input元素 语法格式：
`<input type="">`

type属性的可选值有：
- text 单行文本框

属性：name 文本框名称
- value 文本框的初始值
- size 文本框的长度
- maxlength 可输入字符串最大的长度
- radio 单选框

属性：name 单选框名称
- value 内部值
- checked 默认选定
- checkbox 复选框

属性：name 复选框名称
- value 内部值
- checked 默认选定
- reset 重置按钮
- submit 确定按钮

属性：name 按钮名称
- value 显示在按钮上的文字
- password 密码框
属性与文本框的属性完全相同
file 文件域

属性：name文件域名称
- size 文件域的长度
- maxlength 文件域可接受的字符数量的上限
- hidden 隐藏域

属性：name 隐藏域名称
- value 内定值
- image 图片域

属性：name 所要代表的按钮，可以是submit,reset,或其他.
src 按钮图片的url 地址

列表框 `<select>`
语法格式：

```html
<select>
.....
<option>....</option>
.....
</select>
```

select元素
语法格式：`<select name="" size=""multiple></select>`
- name 指定列表框的名字
- size 指定列表框显示列表项的条数，如果指定了该参数，select元素是个列表，否则是一个下拉列表框
- multiple 指定了这个参数，则表示该列表框可选择多项，否则只可选择一项

option属性

语法格式：
`<option value="" selected></option>`
- value 该列表项的值
- selected 如果设定了这个参数，默认为选定这一项

多行文本框`<textarea>`
```html
<textarea name="" cols="" rows="" wrap="off/physical/virtual"></textarea>
```

属性：
- name文本框的名称
- cols文本框的宽度
- rows文本框的高度
- wrap文本框的折行方式可选值有：
- off不保存换行信息
- physical强迫浏览器在发送信息到web服务器端时必须将多行文本框的文字一行一行的送出，
- virtual送出连续成串的字除非使用者按回车。


虚线
```html
<textarea STYLE="border:1px dashed pink"></textarea>
```
实线
```html
<textarea STYLE="border:1px solid pink"></textarea>
```




网页结构一般都包含文档声明DOCTYPE，并且在head中的meta应该包含编码格式、关键字、网页描述信息。

### 网页结构

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Hello World</title>
</head>
<body>
</body>
```

（1）结构化元素包括：

```html
< header >, < nav >, < article >, < section >, < aside >, < footer >。
```

（2）元素级别：都是block级别元素，不包含样式，只用于结构化，每个页面可多次使用。
（3）元素说明：
>header描述头部信息，
nav用于导航模块，
article用于可重新覆盖的新闻类内容块，section模块化，
aside页面左或右模块，
footer底脚模块。

## 常用布局元素


div：流布局使用；

span：文字块使用。

JD首页的meta声明包含：

- charset 编码格式
- description网站描述
- Keywords关键字

```html
< meta charset="gbk" />
< meta name="description" content="京东JD.COM-专业的综合网上购物商城,销售家电等数万个品牌优质商品.便捷、诚信的服务，为您提供愉悦的网上购物体验!">
< meta name="Keywords" content="网上购物,网上商城,手机,笔记本,电脑">
```

## 文字类元素

（1）加粗元素：strong、b。例如：

```html
< p>< strong>Caution:< /strong> Falling rocks.< /p>< p>This recipe calls for < b>bacon< /b> and < b>baconnaise< /b>.< /p>
```

（2）倾斜元素：和。例如：

```html
< !-- Stressed emphasis -- >
< p>I < em>love< /em> Chicago!< /p>
< !-- Alternative voice or tone -->
< p>The name < i>Shay< /i> means a gift.< /p>
```

## 自关闭元素

```html
< br>
< embed>
< hr>
< img>
< input>
< link>
< meta>
< param>
< source>
< wbr>
```

## 页面内跳转

如果需要跳转到页面指定的位置，可在该位置设置元素的id属性，然后为链接添加href="#id"。例如：

```html
< body id="top" >
...
< a href="#top" >Back to top< /a >
...
< /body >
```
