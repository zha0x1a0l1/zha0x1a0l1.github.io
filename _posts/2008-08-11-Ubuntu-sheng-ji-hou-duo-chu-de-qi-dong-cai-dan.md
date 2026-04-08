---
title: Ubuntu升级后多出的启动菜单
date: '2008-08-11 00:00:00'
slug: Ubuntu-sheng-ji-hou-duo-chu-de-qi-dong-cai-dan
categories:
- 网络
tags:
- 网站
- Linux
---
在官方网站下载Ubuntu 8.04桌面版的Linux内核是2.6.24-19，安装好后把系统升级到最新，内核变成了2.6.24-20。这是在开机的选择启动项里就多出了两个启动选择，如下图：
[![](/assets/images/2008/08/1111.jpg)](/uploads/2008/08/1111.jpg)

而在通常情况下，我们就没必要再进入旧的内核系统了，我们把不需要的两个启动选择项删掉。

在终端。备份下这个文件，防止出错:
> sudo cp /boot/grub/menu.lst /boot/grub/menu.lst.backup

编辑这个文件:
> sudo gedit /boot/grub/menu.lst

找到如下文字：
 ## ## End Default Options ##

title		Ubuntu 8.04.1, kernel 2.6.24-20-generic
root		(hd0,8)
kernel		/boot/vmlinuz-2.6.24-20-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro quiet splash locale=zh_CN
initrd		/boot/initrd.img-2.6.24-20-generic
quiet

title		Ubuntu 8.04.1, kernel 2.6.24-20-generic (recovery mode)
root		(hd0,8)
kernel		/boot/vmlinuz-2.6.24-20-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro single
initrd		/boot/initrd.img-2.6.24-20-generic

title		Ubuntu 8.04.1, kernel 2.6.24-19-generic
root		(hd0,8)
kernel		/boot/vmlinuz-2.6.24-19-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro quiet splash locale=zh_CN
initrd		/boot/initrd.img-2.6.24-19-generic
quiet

title		Ubuntu 8.04.1, kernel 2.6.24-19-generic (recovery mode)
root		(hd0,8)
kernel		/boot/vmlinuz-2.6.24-19-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro single
initrd		/boot/initrd.img-2.6.24-19-generic

title		Ubuntu 8.04.1, memtest86+
root		(hd0,8)
kernel		/boot/memtest86+.bin
quiet

### END DEBIAN AUTOMAGIC KERNELS LIST
把上面画线的文字删除，保存退出后就好了。

---


