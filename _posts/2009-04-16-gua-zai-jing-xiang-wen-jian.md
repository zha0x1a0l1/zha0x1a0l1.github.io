---
title: 挂载镜像文件
date: '2009-04-16 00:00:00'
slug: gua-zai-jing-xiang-wen-jian
categories:
- 网络
tags:
- Linux
- 软件
---
120、Access ISO images as if they’re disk drives（挂载镜像文件）
A better way is to mount the ISO image just like you an actual disk. To do so, open a terminal window and type the following (this assumes the file ubuntu.iso is in your /home folder):
（挂载镜像文件，就像打开本地磁盘一样。假设你将镜像文件放到了主文件夹下，在终端输入）
$ sudo mkdir /media/ISO
$ sudo mount -o loop ~/ubuntu.iso /media/ISO
Once the ISO image is mounted, an icon for it will automatically appear on the desktop.
（挂载后，你就能在桌面上看到相应的图标了）
To unmount the image, type sudo umount /media/ISO in the terminal window.
（使用sudo umount /media/ISO 卸载镜像文件）

---


