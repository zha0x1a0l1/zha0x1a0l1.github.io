---
title: Ubuntu9.04无法开启桌面特效和3D特效
date: '2009-04-25 00:00:00'
slug: Ubuntu904-wu-fa-kai-qi-zhuo-mian-te-xiao-he-3D-te-xiao
categories:
- 科技
tags:
- jekyll
- Linux
- 服务器
- 科技
- Google
---
我的电脑是intel X3100的集成显卡，安装9.04以前的版本时都无须多设置就能直接开启桌面特效和3D特效。上次从8.10直接[升级Ubuntu到9.04 Alpha5](http://blog.zhaoxiao.li/archives/2299.html)也没有出现问题，而这次却不行了。折腾了打半夜，终于google到设置方法：
1、使用2.6.30rc3linux内核，按照下列顺序下载并安装：
- 32bit -
Kernel Header:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... c3_all.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-headers-2.6.30-020630rc3_2.6.30-020630rc3_all.deb)
Kernel Header Generic:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... 3_i386.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-headers-2.6.30-020630rc3-generic_2.6.30-020630rc3_i386.deb)
Kernel Header Image:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... 3_i386.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-image-2.6.30-020630rc3-generic_2.6.30-020630rc3_i386.deb)

- 64bit -
Kernel Header:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... c3_all.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-headers-2.6.30-020630rc3_2.6.30-020630rc3_all.deb)
Kernel Header Generic:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... _amd64.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-headers-2.6.30-020630rc3-generic_2.6.30-020630rc3_amd64.deb)
Kernel Header Image:
[http://kernel.ubuntu.com/~kernel-ppa/ma ... _amd64.deb](http://kernel.ubuntu.com/~kernel-ppa/mainline/v2.6.30-rc3/linux-image-2.6.30-020630rc3-generic_2.6.30-020630rc3_amd64.deb)
（如果下载速度慢，从这个镜像下载：[http://myubuntu.ca/download/mirror/kernel/2.6.30rc3/](http://myubuntu.ca/download/mirror/kernel/2.6.30rc3/)）

2、运行sudo gedit /etc/X11/xorg.conf
把
 Section "Device"
Identifier "Configured Video Device"
EndSection
修改为
 Section "Device"
Identifier "intel"
EndSection
把
 Section "Screen"
Identifier "Default Screen"
Monitor "Configured Monitor"
Device "Configured Video Device"
EndSection
修改为
 Section "Screen"
Identifier "Default Screen"
Monitor "Configured Monitor"
Device "intel"
EndSection
3、卸载现有驱动
sudo apt-get remove xserver-xorg-video-intel
4、重新安装驱动
sudo apt-get install xserver-xorg-video-intel
5、修改compiz的配置
sudo gedit /etc/xdg/compiz/compiz-manager
新起一行，增加SKIP_CHECKS=yes， 保存
6、运行 sudo apt-get install compizconfig-settings-manager
安装compiz的配置管理器
7、重启系统，打开compiz fusion icon，在window manager中选择 compiz
8、成功打开桌面效果和3D
（以上在神舟F2370 X3100显卡上测试成功）
原帖地址：[http://forum.ubuntu.org.cn/viewtopic.php?f=94&t=114571&start=15](http://forum.ubuntu.org.cn/viewtopic.php?f=94&t=114571&start=15)

---


