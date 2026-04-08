---
title: 将Nautilus更改为轻量级文件管理器Thunar
date: '2009-04-08 00:00:00'
slug: jiang-Nautilus-geng-gai-wei-qing-liang-ji-wen-jian-guan-li-qi-Thunar
categories:
- 网络
tags:
- Google
- 软件
---
92、Switch to a lightweight file manager（将Nautilus更改为轻量级文件管理器Thunar）

1. Start Synaptic and search for and install the thunar and thunararchive-plugin packages. After installation, you can run Thunar by typing thunar in a terminal window.
(用新立得搜索并安装 thunar 和 thunararchive-plugin 。)
2. To cause Thunar to open whenever you click an entry on the Places menu, you’ll need to edit a configuration file: open a terminal window and type the following:
(编辑configuration文件，在终端里输入：)

$ gksu gedit /usr/share/applications/nautilus-folder-handler.desktop
Scroll to the bottom of the file and look for the line that reads Exec=nautilus --no-desktop %U. Change it so it reads Exec=thunar %U.
(在底部找到Exec=nautilus --no-desktop %U 这行，将它替换为Exec=thunar %U ，保存后退出。)

---


