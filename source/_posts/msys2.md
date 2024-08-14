---
title: msys2
date: 2024-05-03 12:05:32
cover: 
tags: 
mathjax: false
---

<!-- more -->
## 1. Environments
  
| Name           | Prefix        | Toolchain | Architecture | C Library | C++ Library | Package prefix           | pacboy Package suffix |
| -------------- | ------------- | --------- | ------------ | --------- | ----------- | ------------------------ | --------------------- |
| **MSYS**       | `/usr`        | gcc       | x86_64       | cygwin    | libstdc++   |                          |                       |
| **UCRT64**     | `/ucrt64`     | gcc       | x86_64       | ucrt      | libstdc++   | mingw-w64-ucrt-x86_64-   | u                     |
| **CLANG64**    | `/clang64`    | llvm      | x86_64       | ucrt      | libc++      | mingw-w64-clang-x86_64-  | c                     |
| **CLANGARM64** | `/clangarm64` | llvm      | aarch64      | ucrt      | libc++      | mingw-w64-clang-aarch64- | a                     |
| **CLANG32**    | `/clang32`    | llvm      | i686         | ucrt      | libc++      | mingw-w64-clang-i686-    | z                     |
| **MINGW64**    | `/mingw64`    | gcc       | x86_64       | msvcrt    | libstdc++   | mingw-w64-x86_64-        | x                     |
| **MINGW32**    | `/mingw32`    | gcc       | i686         | msvcrt    | libstdc++   | mingw-w64-i686-          | i                     |

## 2. Updating MSYS2
```sh
pacman -Suy
```

## 3. Finding a package
```sh
pacman -Ss
```

## 4. Installing a package
```sh
# pacboy
pacman -S pactoys
pacman -S vim
# 当前环境包
pacboy -S package:p

# 7-zip
pacman -S mingw-w64-ucrt-x86_64-7zip
# gcc
pacman -S mingw-w64-ucrt-x86_64-toolchain
# cmake
pacman -S mingw-w64-ucrt-x86_64-cmake
pacman -S mingw-w64-ucrt-x86_64-qemu
# clang
pacman -S mingw-w64-ucrt-x86_64-clang
pacman -S mingw-w64-ucrt-x86_64-clang-tools-extra
pacman -S mingw-w64-ucrt-x86_64-lldb
pacman -S mingw-w64-ucrt-x86_64-lld
pacman -S mingw-w64-ucrt-x86_64-python-conan
pacman -S mingw-w64-ucrt-x86_64-sqlite3
pacman -S mingw-w64-ucrt-x86_64-putty
pacman -S mingw-w64-ucrt-x86_64-ruby
pacman -S mingw-w64-ucrt-x86_64-aria2
pacman -S mingw-w64-ucrt-x86_64-dosbox
pacman -S mingw-w64-ucrt-x86_64-yasm
pacman -S mingw-w64-ucrt-x86_64-nasm
pacman -S mingw-w64-ucrt-x86_64-nodejs
pacman -S mingw-w64-ucrt-x86_64-mosquitto
pacman -S mingw-w64-ucrt-x86_64-paho.mqtt.c
pacman -S mingw-w64-ucrt-x86_64-graphviz
pacman -S mingw-w64-ucrt-x86_64-imagemagick
pacman -S mingw-w64-ucrt-x86_64-nsis
# qt-creator
pacman -S mingw-w64-ucrt-x86_64-qt-creator
# texstudio
pacman -S mingw-w64-ucrt-x86_64-texstudio
# texlive
pacman -S mingw-w64-ucrt-x86_64-texlive-scheme-gust
pacman -S mingw-w64-ucrt-x86_64-opencv
pacman -S mingw-w64-ucrt-x86_64-gimp
pacman -S mingw-w64-ucrt-x86_64-krita
pacman -S mingw-w64-ucrt-x86_64-kimageformats-qt5
pacman -S mingw-w64-ucrt-x86_64-blender

pacman -S mingw-w64-ucrt-x86_64-kicad
pacman -S mingw-w64-ucrt-x86_64-kicad-meta
pacman -S mingw-w64-ucrt-x86_64-kicad-doc-zh
# https://openscad.org/documentation.html
pacman -S mingw-w64-ucrt-x86_64-openscad
# https://wiki.freecad.org/Getting_started
pacman -S mingw-w64-ucrt-x86_64-freecad

pacman -S mingw-w64-ucrt-x86_64-kdenlive
pacman -S mingw-w64-ucrt-x86_64-hugo
pacman -S mingw-w64-ucrt-x86_64-go
pacman -S mingw-w64-ucrt-x86_64-rust
pacman -S mingw-w64-ucrt-x86_64-perl
pacman -S mingw-w64-ucrt-x86_64-lua
```

## 5. Uninstalling a package
```sh
pacman -R
```



- [msys2](https://www.msys2.org/)
- [MSYS2 Packages](https://packages.msys2.org/)
- [pacman](https://wiki.archlinux.org/title/Pacman)
- [将代码升级到ucrt](https://learn.microsoft.com/zh-cn/cpp/porting/upgrade-your-code-to-the-universal-crt?view=msvc-170)

- [cygwin](https://cygwin.com/index.html)