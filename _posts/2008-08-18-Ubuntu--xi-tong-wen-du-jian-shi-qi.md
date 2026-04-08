---
title: Ubuntu-系统温度监视器
date: '2008-08-18 00:00:00'
slug: Ubuntu--xi-tong-wen-du-jian-shi-qi
categories:
- 科技
tags:
- Apple
- Linux
- 软件
---
![](/assets/images/2008/08/ubuntulogo.png)
夏天天热，最担心的是本本的温度，所以找个温度监视器，来随时关注系统的温度状况。
[![](/assets/images/2008/08/e697a0e6a087e9a298.jpg)](/uploads/2008/08/e697a0e6a087e9a298.jpg)
安装方法：
安装HardWare Sensors Monitor:
sudo apt-get install sensors-applet
在面板上你想要插入的地方点右键，选择“添加到面板“，找到
[![](/assets/images/2008/08/asf.jpg)](/uploads/2008/08/asf.jpg)
这时在面板上就能显示出CPU的温度了。
安装硬盘温度监控：
sudo apt-get install hddtemp
然后在刚刚新建立的CPU温度的图标处点右键，选择“Preference“，然后选择"Sensors",找到“hddtemp”选项并展开，将其Enabled选项够选。
[![](/assets/images/2008/08/123456.png)](/uploads/2008/08/123456.png)

这样，就能看到硬盘的温度了。

---


