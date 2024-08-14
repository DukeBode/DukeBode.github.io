---
title: Cshape
date: 2022-03-19 19:26:55
tags:
  - cshape
---
## 1. 人名币转大写

<!-- more -->

```cshape
decimal v = decimal.Parse("123.00");
            var s = v.ToString("#L#E#D#C#K#E#D#C#J#E#D#C#I#E#D#C#H#E#D#C#G#E#D#C#F#E#D#C0.0B0A/");
            var d = Regex.Replace(s, @"(((?<=^-)|(^[^-]))[^1-9]*((?=[1-9])|((?<c>0\.)[^1-9]*(?=/$))))|((?<=[1-9]A)/)|((?<z>0)[0A-E]*((?=[1-9])|(?<-z>(?=[F-L\./]|$))))|((?<b>[F-L])(?<z>0)[0A-L]*(?=[1-9]|(?<-z>(?=[\./]|$))))", "${b}${z}${c}");
            var r = Regex.Replace(d, ".", m => "正，负元整零壹贰叁肆伍陆柒捌玖拾屲亗岌岄岪峘分角拾佰仟万亿兆京垓秭穰沟涧正载极"[m.Value[0] - '+'].ToString());
```

## 2. 创建桌面快捷方式

```c#
        /// <summary>
        /// 创建桌面快捷键
        /// </summary>
        /// <param name="LnkName">快捷键名称</param>
        /// <param name="AssemblyFullPath">程序集的完整路径</param>
        /// <param name="IconLocation">图标位置</param>
        /// <param name="Description">描述</param>
        /// <returns></returns>
        public static bool CreateDesktopShortcut(string LnkName, string AssemblyFullPath, string IconLocation = null, string Description = null)
        {
            string DesktopLnkPath = Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.Desktop), $"{LnkName}.lnk");
            if (File.Exists(DesktopLnkPath)) return true;
            IWshRuntimeLibrary.IWshShortcut shortcut = new IWshRuntimeLibrary.WshShell().CreateShortcut(DesktopLnkPath);
            shortcut.WorkingDirectory = Path.GetDirectoryName(AssemblyFullPath);
            shortcut.TargetPath = AssemblyFullPath;
            shortcut.WindowStyle = 1;
            shortcut.Description = Description;
            shortcut.IconLocation = IconLocation ?? AssemblyFullPath;
            shortcut.Save();
            return true;
        }
```

## 3. WINFORM判断是否处于设计模式

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

