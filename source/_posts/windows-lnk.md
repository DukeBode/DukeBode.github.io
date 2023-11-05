---
title: windows 快捷方式
date: 2021-08-10 10:15:39
tags:
  - Windows
  - cshape
---

<!-- more -->

C#

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