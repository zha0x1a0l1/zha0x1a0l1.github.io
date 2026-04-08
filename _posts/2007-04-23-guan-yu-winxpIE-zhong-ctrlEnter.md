---
title: 关于winxp IE中ctrl+Enter
date: '2007-04-23 00:00:00'
slug: guan-yu-winxpIE-zhong-ctrlEnter
categories:
- 科技
tags: []
---
在winxp IE中,按快捷键ctrl+Enter，IE会自动输入www.网址名称.com.cn，那么，我们如何让他变成www.网址名称.com呢？

IE6.0

第一步：在资源管理器中将“c:windowssystem32”文件夹下的BROWSELC.DLL的文件备份（便于出错后修复）。

第二步：使用EXESCOPE打开BROWSELC.DLL，在“资源”→“字串表”下的809处找到 12936， 把“12936.WWW.%S.CO.CN”改为“12936.WWW.%S.COM”，保存，这样问题就解决了。

IE7.0

用PE Explorer打开 C:Windowssystem32zh-cn 目录下的 ieframe.dll.mui ，找到“字符串”下的“809”，里面的12936字符串就是自动补全的网址了，去掉结尾的.cn，保存 ieframe.dll.mui 。

这样打开IE7，按下Ctrl＋Enter就是.com结尾了，这样方便多了。

---


