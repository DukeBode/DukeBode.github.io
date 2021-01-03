---
title: html
date: 2017-09-07 13:01:35
cover:
tags:
  - 前端
---

HTML (HyperText Markup Language) is the most basic building block of the Web. It defines the meaning and structure of web content.

<!-- more -->

跑马灯
```html
<marquee>...</marquee>普通卷动
<marquee behavior=slide>...</marquee>滑动
<marquee behavior=scroll>...</marquee>预设卷动
<marquee behavior=alternate>...</marquee>来回卷动
<marquee direction=down>...</marquee>向下卷动
<marquee direction=up>...</marquee>向上卷动
<marquee direction=right></marquee>向右卷动
<marquee direction=’left’></marquee>向左卷动
<marquee loop=2>...</marquee>卷动次数
<marquee width=180>...</marquee>设定宽度
<marquee height=30>...</marquee>设定高度
<marquee bgcolor=FF0000>...</marquee>设定背景颜色
<marquee scrollamount=30>...</marquee>设定滚动速度
<marquee scrolldelay=300>...</marquee>设定卷动时间
<marquee onmouseover="this.stop()">...</marquee>鼠标经过上面时停止滚动
<marquee onmouseover="this.start()">...</marquee>鼠标离开时开始滚动
<!>字体效果
<h1>...</h1>标题字(最大)
<h6>...</h6>标题字(最小)
<b>...粗体字
<strong>...</strong>粗体字(强调) （同上效果略同）
<i>...</i>斜体字
<em>...</em>斜体字(强调)
<dfn>...</dfn>斜体字(表示定义)
<u>...</u>底线
<ins>...</ins>底线(表示插入文字)
<strike>...</strike>横线
<s>...</s>删除线
<del>...</del>删除线(表示删除)
<kbd>...</kbd>键盘文字
<tt>...</tt> 打字体
<xmp>...</xmp>固定宽度字体(在文件中空白、换行、定位功能有效)
<plaintext>...</plaintext>固定宽度字体(不执行标记符号)
<listing>...</listing> 固定宽度小字体
<font color=00ff00>...</font>字体颜色
<font size=1>...</font>最小字体
<font style =’font-size:100 px’>...</font>无限增大
区断标记
<hr>水平线
<hr size=’9’>水平线(设定大小)
<hr width=’80%’>水平线(设定宽度)
<hr color=’ff0000’>水平线(设定颜色)
<br>(换行)
<nobr>...</nobr>水域(不换行)
...

水域(段落)

<center>...</center>置中
<!>连结格式
<base href=位址>(预设好连结路径)
<a href=位址></a>外部连结
<a href=位址 target=’_blank’></a>外部连结(另开新视窗)
<a href=位址 target=’_top’></a>外部连结(全视窗连结)
<a href=位址 target=’页框名’></a>外部连结(在指定页框连结)
<!>贴图/音乐
<img src=图片位址>贴图
<img src=图片位址 width=’180’>设定图片宽度
<img src=图片位址 height=’30’>设定图片高度
<img src=图片位址 alt=’提示文字’>设定图片提示文字
<img src=图片位址’ border=’1’>设定图片边框
<bgsound src=MID音乐档位址>背景音乐设定
<!>表格语法
<table aling=left>...</table>表格位置,置左
<table aling=center>...</table>表格位置,置中
<table background=图片路径>...</table>背景图片的URL=就是路径网址
<table border=边框大小>...</table>设定表格边框大小(使用数字)
<table bgcolor=颜色码>...</table>设定表格的背景颜色
<table borderclor=颜色码>...</table>设定表格边框的颜色
<table borderclordark=颜色码>...</table>设定表格暗边框的颜色
<table borderclorlight=颜色码>...</table>设定表格亮边框的颜色
<table cellpadding=参数>...</table>指定内容与格线之间的间距(使用数字)
<table cellspacing=参数>...</table>指定格线与格线之间的距离(使用数字)
<table cols=参数>...</table>指定表格的栏数
<table frame=参数>...</table>设定表格外框线的显示方式
<table width=宽度>...</table>指定表格的宽度大小(使用数字)
<table height=高度>...</table>指定表格的高度大小(使用数字)
<td colspan=参数>...</td>指定储存格合并栏的栏数(使用数字)
<td rowspan=参数>...</td>指定储存格合并列的列数(使用数字)
分割视窗
<frameset cols="20%,*">左右分割,将左边框架分割大小为20%右边框架的大小浏览器会自动调整
<frameset rows="20%,*">上下分割,将上面框架分割大小为20%下面框架的大小浏览器会自动调整
<frameset cols="20%,*">分割左右两个框架
<frameset cols="20%,*,20%">分割左中右三个框架
<分割上下两个框架
<frameset rows="20%,*,20%">分割上中下三个框架
属性：
cols 垂直切割窗口（如左右分割两个窗口）接受整数值，百分数，*（*代表占用余下空间）数值的个数代表分成的部分数目，要以逗号分隔。例：cols="30,*,50%"可以 切成三个视窗，第一部分是30像素（pixels）为绝对分割，第二部分是当分配完第一和第三视图后剩下的空间，第三部分则占整个窗口的50%宽度，为相对分割。
rows 就是横向切割，将窗口上下分开，数值设置同上。
以上两属性尽量不要在同一个<frameset>标记中，因为王井（netscape）不支持，尽量采用多重分割。
frameborder 设置框架的边框，其值有0不要边框，1要边框。
border 设置框架边框厚度
framespacing 表示框架与框架间保留空白的距离
frame 元素（单标签）
语法格式：
<frame name="" src="url" scrolling="yes/no" noresize>
属性：
name 框架名称，指定框架来做连接的目标窗口。
src 框架中要显示的网页文当url地址，每个个框架要对应一个html文挡。
scrolling 是否显示滚动条，yes/no,auto是自动。
noresize 设置不让使用者改变这个框架的大小，
noframe元素
指定当使用了框架的页面在不支持框架的浏览器中打开时显示的信息
语法格式：
<noframe>
......
</noframe>

表单<form></form>
语法格式：
<form action="url" method="get/post">
....
<input type=submit><input type=reset>
</form>
method有两种提交方式get,post
action 是指明处理该表单的程序位置，这样表单所填的资料才能传给cgi做处里，可设定此参数为action="mailto:lwr8494@163.com" 这样此表单所填的资料将会发送到这个邮箱地址。
method 是指传送信息给cgi等网络程序的方式。可选post方法， get方法，post方法容许传送大量信息。get方法只接受低于1k的信息。
申请表单用的是post搜索引擎用的是get
 
<! - - ... - -> 注解
<A HREF TARGET> 指定超连结的分割视窗
<A HREF=#锚的名称> 指定锚名称的超连结
<A HREF> 指定超连结
<A NAME=锚的名称> 被连结点的名称
<ADDRESS>....</ADDRESS> 用来显示电子邮箱地址
<B> 粗体字
<BASE TARGET> 指定超连结的分割视窗
<BASEFONT SIZE> 更改预设字形大小
<BGSOUND SRC> 加入背景音乐
<BIG> 显示大字体
<BLINK> 闪烁的文字
<BODY TEXT LINK VLINK> 设定文字颜色
<BODY> 显示本文
<BR> 换行
<CAPTION ALIGN> 设定表格标题位置
<CAPTION>...</CAPTION> 为表格加上标题
<CENTER> 向中对齐
<CITE>...<CITE> 用於引经据典的文字
<CODE>...</CODE> 用於列出一段程式码
<COMMENT>...</COMMENT> 加上注解
<DD> 设定定义列表的项目解说
<DFN>...</DFN> 显示"定义"文字
<DIR>...</DIR> 列表文字标签
<DL>...</DL> 设定定义列表的标签
<DT> 设定定义列表的项目
<EM> 强调之用
<FONT FACE> 任意指定所用的字形
<FONT SIZE> 设定字体大小
<FORM ACTION> 设定户动式表单的处理方式
<FORM METHOD> 设定户动式表单之资料传送方式
<FRame MARGINHEIGHT> 设定视窗的上下边界
<FRame MARGINWIDTH> 设定视窗的左右边界
<FRame NAME> 为分割视窗命名
<FRame NORESIZE> 锁住分割视窗的大小
<FRame SCROLLING> 设定分割视窗的卷轴
<FRame SRC> 将HTML档加入视窗
<FRameSET COLS> 将视窗分割成左右的子视窗
<FRameSET ROWS> 将视窗分割成上下的子视窗
<FRameSET>...</FRameSET> 划分分割视窗
<H1>~<H6> 设定文字大小
<HEAD> 标示文件资讯
<HR> 加上分格线
<HTML> 文件的开始与结束
<I> 斜体字
<IMG ALIGN> 调整图形影像的位置
<IMG ALT> 为你的图形影像加注
<IMG DYNSRC LOOP> 加入影片
<IMG HEIGHT WIDTH> 插入图片并预设图形大小
<IMG HSPACE> 插入图片并预设图形的左右边界
<IMG LOWSRC> 预载图片功能
<IMG SRC BORDER> 设定图片边界
<IMG SRC> 插入图片
<IMG VSPACE> 插入图片并预设图形的上下边界
<INPUT TYPE NAME value> 在表单中加入输入栏位
<ISINDEX> 定义查询用表单
<KBD>...</KBD> 表示使用者输入文字
<LI TYPE>...</LI> 列表的项目 ( 可指定符号 )
<MARQUEE> 跑马灯效果
<MENU>...</MENU> 条列文字标签
<meta NAME="REFRESH" CONTENT URL> 自动更新文件内容
<MULTIPLE> 可同时选择多项的列表栏
<NOFRame> 定义不出现分割视窗的文字
<OL>...</OL> 有序号的列表
<OPTION> 定义表单中列表栏的项目
<P ALIGN> 设定对齐方向
<P> 分段
<PERSON>...</PERSON> 显示人名
<PRE> 使用原有排列
<SAMP>...</SAMP> 用於引用字
<select >...</select > 在表单中定义列表栏
<SMALL> 显示小字体
<STRIKE> 文字加横线
<STRONG> 用於加强语气
<SUB> 下标字
<SUP> 上标字
<TABLE BORDER=n> 调整表格的宽线高度
<TABLE CELLPADDING> 调整资料栏位之边界
<TABLE CELLSPACING> 调整表格线的宽度
<TABLE HEIGHT> 调整表格的高度
<TABLE WIDTH> 调整表格的宽度
<TABLE>...</TABLE> 产生表格的标签
<TD ALIGN> 调整表格栏位之左右对齐
<TD BGCOLOR> 设定表格栏位之背景颜色
<TD COLSPAN ROWSPAN> 表格栏位的合并
<TD NOWRAP> 设定表格栏位不换行
<TD VALIGN> 调整表格栏位之上下对齐
<TD WIDTH> 调整表格栏位宽度
<TD>...</TD> 定义表格的资料栏位
<TEXTAREA NAME ROWS COLS> 表单中加入多少列的文字输入栏
<TEXTAREA WRAP> 决定文字输入栏是自动否换行
<TH>...</TH> 定义表格的标头栏位
<TITLE> 文件标题
<TR>...</TR> 定义表格美一行
<TT> 打字机字体
<U> 文字加底线
<UL TYPE>...</UL> 无序号的列表 ( 可指定符号 )
<var>...</var> 用於显示变数
BlockQuotc文本缩进
表示颜色的有三种方式；
1，16进制颜色代码
语法：#RRGGBB
例：<font color="#ff0000">红色</font>
2，10进制RGB码
语法：RGB（RRR，GGG，BBB）
例：<font color="rgb(255,000,000)">红色</font>
3,直接用颜色的英文名称
例：<font color="red">红色</font>
<body>.....</body>属性可分为三种：
1，背景属性
包括：bgcolor,background
2,文字属性：
包括：text,link,alink,vlink,
3,留白属性：
其中分为：leftmargin,topmargin
.bgcolor背景色
语法格式：<body bgcolor="#ff0000">
.background背景图案。
语法格式：<body background="url">
.text文本颜色（非连接文字颜色）
.link连接文字颜色（可连接文字颜色）
.alink活动连接文字颜色（正被点击的可连接文字的颜色）
.vlink已访问连接文字颜色）（已经点击访问过的可连接文字的颜色）

语法格式：<body text="color" link="color" alink="color" vlink="color">
.leftmargin 页面左侧的留白距离
.topmargin 页面顶部的留白距离

语法格式：<body leftmargin="value" topmargin="value">
注：value为长度值为数字
align 属性
语法：<h2 align="?">文字</h2>
其属性有三种：left靠左,center居中,right靠右
〈p〉
为段落标记，可利用以上属性对整个段落进行设置
```

`<br>`为换行标记

<nobr></nobr>为不换行标记 放在文字两边即可
例：
```html
<body>
<h3>江南逢李龟年</h3>
歧王宅里寻常见<br>
催九堂前几度闻<br>
正是江南好风景<br>
落花时节又逢君
</body>
```