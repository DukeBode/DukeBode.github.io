---
title: URL Protocol
date: 2021-08-10 10:07:39
tags:
---

<!-- more -->

C#

```C#
        /// <summary>
        /// 为指定程序注册URL Protocol,方便浏览器调用
        /// </summary>
        /// <param name="ProtocolName">协议名称</param>
        /// <param name="path">程序的完整路径</param>
        /// <param name="Exists">写入前存在状态</param>
        /// <param name="Override">如果存在是否重写数据，默认 false 不重写</param>
        /// <exception cref="ArgumentException">参数异常</exception>
        public static void RegisterUrlProtocol(string ProtocolName, string path, out bool Exists, bool Override = false)
        {
            if (string.IsNullOrWhiteSpace(ProtocolName))
            {
                throw new ArgumentException("协议名称为空！！！");
            }

            Microsoft.Win32.RegistryKey key = Microsoft.Win32.Registry.ClassesRoot.OpenSubKey(ProtocolName, true);
            Exists = key != null;
            if (Exists && !Override)
            {
                return;
            }
            if (string.IsNullOrWhiteSpace(path))
            {
                throw new ArgumentException("关联程序路径为空！！！");
            }

            if (!File.Exists(path))
            {
                throw new ArgumentException("关联程序不存在！！！");
            }
            key = key ?? Microsoft.Win32.Registry.ClassesRoot.CreateSubKey(ProtocolName);
            key.SetValue("", $"{ProtocolName} Protocol", Microsoft.Win32.RegistryValueKind.String);
            key.SetValue("URL Protocol", path, Microsoft.Win32.RegistryValueKind.String);
            key.CreateSubKey("DefaultIcon").SetValue("", $"{path},1", Microsoft.Win32.RegistryValueKind.String);
            key.CreateSubKey("shell").CreateSubKey("open").CreateSubKey("command")
                .SetValue("", $"\"{path}\" \"%1\"", Microsoft.Win32.RegistryValueKind.String);
        }
```