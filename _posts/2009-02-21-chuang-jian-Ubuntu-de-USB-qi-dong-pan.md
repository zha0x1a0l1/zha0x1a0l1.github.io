---
title: 创建Ubuntu的USB启动盘
date: '2009-02-21 00:00:00'
slug: chuang-jian-Ubuntu-de-USB-qi-dong-pan
categories:
- 科技
tags:
- 科技
- Linux
---
在Ubuntu8.10版本中，在“系统-系统管理”中有一个Make USB Startup Disk功能，最近才发现，这个功能真是超级好。
至少有两个好处：
1、带着自己配置的Ubuntu系统到处跑，只需带个USB而不是以前的光盘。
2、在装系统的时候，没必要刻盘了，直接用USB安装，节省了光盘，也给没有刻录机的朋友带来很大方便。
而这，所有的一起，只需要一个大于1G的USB而已。
安装使用方法：
将U盘插到电脑上，依次打开“系统-系统管理-Make USB Disk”，
![](/assets/images/2009/02/2.jpg)
点击“Others”，浏览到你要加载的镜像文件，调整“Stored In reserved extra space”的how much tab中的大小（这个大小是用来保存你的私人文件的，USB不同于光盘的地方就是你所操作过文件和配置都能保存）
![](/assets/images/2009/02/3.jpg)
然后点击"Make Startup disk"，开始复制文件到USB中
![](/assets/images/2009/02/1.jpg)
整个过程大概需要10分钟左右的样子，这应取决于系统运行的快慢。
制作USB启动盘的好处：
1、你可以带一个USB而不是一个光盘到处跑。
2、你所有的私人文件，配置都可以保存到USB中，真正的移动系统。
3、安装系统时，就没有必要刻盘了，可以通过USB安装。
当然，这所有的一起需要你的电脑支持USB启动。现在的电脑应该都支持吧，除非是老古董。

---


