---
title: 人民币转大写
date: 2022-03-19 19:26:55
tags:
---
<!-- more -->

```cshape
decimal v = decimal.Parse("123.00");
            var s = v.ToString("#L#E#D#C#K#E#D#C#J#E#D#C#I#E#D#C#H#E#D#C#G#E#D#C#F#E#D#C0.0B0A/");
            var d = Regex.Replace(s, @"(((?<=^-)|(^[^-]))[^1-9]*((?=[1-9])|((?<c>0\.)[^1-9]*(?=/$))))|((?<=[1-9]A)/)|((?<z>0)[0A-E]*((?=[1-9])|(?<-z>(?=[F-L\./]|$))))|((?<b>[F-L])(?<z>0)[0A-L]*(?=[1-9]|(?<-z>(?=[\./]|$))))", "${b}${z}${c}");
            var r = Regex.Replace(d, ".", m => "正，负元整零壹贰叁肆伍陆柒捌玖拾屲亗岌岄岪峘分角拾佰仟万亿兆京垓秭穰沟涧正载极"[m.Value[0] - '+'].ToString());
```