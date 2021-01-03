---
title: web-html-meta
date: 2020-01-22 10:46:48
cover:
tags:
  - 前端
---

The HTML `<meta>` element represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` or `<title>`.

<!-- more -->

viewport 

使用元视口代码控制浏览器视口的宽度和缩放比例。

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- 添加 width=device-width 以便与屏幕宽度（以设备无关像素为单位）进行匹配。
- 添加 initial-scale=1 以便将 CSS 像素与设备无关像素的比例设为 1:1。
- 确保在不停用用户缩放功能的情况下，您的网页也可以访问。

除了设置 initial-scale 外，您还可以在视口上设置以下属性：

- minimum-scale
- maximum-scale
- user-scalable

但是，设置后，这些属性可以停用用户缩放视口的功能，可能会造成网页访问方面的问题。