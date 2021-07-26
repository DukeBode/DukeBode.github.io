---
title: Office-Excel
date: 2021-07-26 09:32:24
tags:
---
<!-- more -->

### EXCEL 批量添加图片

```html
<table><img src="图片链接"/>
```
复制html文本，选择性粘贴”，选择Unicode文本。

可用于条码的批量生成，早期有规律的网络图片爬虫。

### EXCEL 图片居中

```vb
Sub dq()
Dim shp As Shape
For Each shp In ActiveSheet.Shapes
shp.Left = (shp.TopLeftCell.Width - shp.Width) / 2 + shp.TopLeftCell.Left
shp.Top = (shp.TopLeftCell.Height - shp.Height) / 2 + shp.TopLeftCell.Top
Next
End Sub
```