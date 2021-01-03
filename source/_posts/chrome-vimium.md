---
title: vimium
date: 2020-01-08 19:29:21
cover:
tags:
---

Vimium is a Chrome extension that provides keyboard-based navigation and control of the web in the spirit of the Vim editor.

<!-- more -->

### vimium 
[官网](https://github.com/philc/vimium)

```Custom key mappings
# Insert your preferred key mappings here.
map h previousTab
map l nextTab

map H scrollLeft
map J scrollPageDown
map K scrollPageUp
map L scrollRight

map gh goBack
map gj scrollToBottom
map gk scrollToTop
map gl goForward
map gt Vomnibar.activateTabSelection

map th firstTab
map tl lastTab
# map tn createTab
map tn Vomnibar.activateInNewTab
map tb Vomnibar.activateBookmarksInNewTab
map tr reload
map tg Vomnibar.activateTabSelection
unmap t

unmap x
map xx restoreTab
map ' removeTab
map xh' closeTabsOnLeft
map xl' closeTabsOnRight
map xo' closeOtherTabs

map u Vomnibar.activateEditUrl

map c LinkHints.activateMode
# map f LinkHints.activateModeToOpenInNewTab
map o LinkHints.activateModeToOpenInNewTab
map mo Vomnibar.activateBookmarksInNewTab
```

```
# w: https://www.wikipedia.org/w/index.php?title=Special:Search&search=%s Wikipedia

# More examples.
#
# (Vimium supports search completion Wikipedia, as
# above, and for these.)
#

# l: https://www.google.com/search?q=%s&btnI I'm feeling lucky...
# y: https://www.youtube.com/results?search_query=%s Youtube
# gm: https://www.google.com/maps?q=%s Google maps
bing: https://www.bing.com/search?q=%s Bing
baidu: https://www.baidu.com/s?wd=%s Baidu
google: https://www.google.com/search?q=%s Google
github: https://github.com/search?q=%s GitHub
weibo: https://s.weibo.com/weibo?q=%s 微博搜索
cqvip: http://www.cqvip.com/main/search.aspx?k=%s 维普期刊
pypi: https://pypi.org/search/?q=%s Python Package Index
te: https://translate.google.cn/#view=home&op=translate&sl=zh-CN&tl=en&text= Google 中译英
x: https://x.cnki.net/kns/brief/Default_Result.aspx?code=SCDB&kw=%s China National Knowledge Infrastructure
# d: https://duckduckgo.com/?q=%s DuckDuckGo
# az: https://www.amazon.com/s/?field-keywords=%s Amazon
# qw: https://www.qwant.com/?q=%s Qwant
```