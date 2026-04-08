---
title: 手工制作清理系统垃圾文件的BAT文件
date: '2006-06-01 00:00:00'
slug: shou-gong-zhi-zuo-qing-li-xi-tong-la-ji-wen-jian-de-BAT-wen-jian
categories:
- 杂项
tags: []
---
新建一个记事本，然后写上
    @echo off
　　echo 正在清除系统垃圾文件，请稍等......
　　del /f /s /q %systemdrive%.tmp
　　del /f /s /q %systemdrive%._mp
　　del /f /s /q %systemdrive%.log
　　del /f /s /q %systemdrive%.gid
　　del /f /s /q %systemdrive%.chk
　　del /f /s /q %systemdrive%.old
　　del /f /s /q %systemdrive%
ecycled.
　　del /f /s /q %windir%.bak
　　del /f /s /q %windir%prefetch.
　　rd /s /q %windir% emp & md %windir% emp
　　del /f /q %userprofile%cookies.
　　del /f /q %userprofile%
ecent.
　　del /f /s /q "%userprofile%Local SettingsTemporary Internet Files."
　　del /f /s /q "%userprofile%Local SettingsTemp."
　　del /f /s /q "%userprofile%
ecent."
　　echo 清除系统垃圾完成！
　　echo. & pause

保存后，把记事本改为 清理垃圾文件.BAT
执行即可马上看到效果哦。 是不是很方便……

---


