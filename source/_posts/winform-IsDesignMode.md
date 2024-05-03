---
title: WINFORM判断是否处于设计模式
date: 2024-05-03 18:59:39
cover: 
tags: 
mathjax: false
---
WINFORM判断是否处于设计模式
<!-- more -->

在设计自定义控件时，经常需要在构造函数或者Load事件中添加初始化代码，但是这些代码在进入窗体设计也会被执行，造成了设计窗口出现异常的情况。  

使用下面的代码，可以让你判断出是否处于窗体设计模式，进而保证代码只会在最终用户使用时才会被执行。  
     
```c#
using System.Diagnostics;
public static bool IsDesignMode()
{
	bool returnFlag = false;
	if (LicenseManager.UsageMode == LicenseUsageMode.Designtime)
	{
		returnFlag = true;
	}
	else if (Process.GetCurrentProcess().ProcessName == "devenv")
	{
	returnFlag = true;
	}
	return returnFlag;
}
```


-  来自 <[https://blog.csdn.net/sleeper1982/article/details/40826497](https://blog.csdn.net/sleeper1982/article/details/40826497)>