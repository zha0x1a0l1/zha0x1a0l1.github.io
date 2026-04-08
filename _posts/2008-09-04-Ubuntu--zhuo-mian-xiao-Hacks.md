---
title: Ubuntu-桌面小Hacks
date: '2008-09-04 00:00:00'
slug: Ubuntu--zhuo-mian-xiao-Hacks
categories:
- 科技
tags:
- Linux
- 软件
---
[![](/assets/images/2008/09/e69caae591bde5908d.jpg)](/uploads/2008/09/e69caae591bde5908d.jpg)
在桌面显示“计算机，主目录，回收站”图标
Ubuntu默认的桌面上是不显示这些图标的，这给操作方面带来一些不便。按“Atl+F2”，调出“运行程序”，输入“gconf-editor”。这个有点像Windows下的注册表。（在这里操作要小心些，这里的操作没有类似于应用，确定的选项，你所作的任何更改系统将自动保存。）依此找到“apps-nautilus-desktop”,分别够选右边窗口的”computer_icon_visible,home_icon_visible,tush_icon_name”,这些图标就会在桌面显示出来。
去掉清空回收站的确认提示
找到“apps-nautilus-preferences-confirm_trash”,将右边的“confirm_tuash”的勾勾掉即可。勾选表示会出现确认提示。
在右键菜单中添加“删除（D）”选项。
找到“apps-nautilus-preferences-enable_delete”，勾选右边的“enable_delete”即可。这样的删除方式是永久删除，而非移动到回收站。等同于shift+delete快捷键。

---


