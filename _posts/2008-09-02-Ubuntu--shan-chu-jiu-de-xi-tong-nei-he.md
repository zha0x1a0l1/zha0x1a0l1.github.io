---
title: Ubuntu-删除旧的系统内核
date: '2008-09-02 00:00:00'
slug: Ubuntu--shan-chu-jiu-de-xi-tong-nei-he
categories:
- 网络
tags:
- Linux
---
Linux内核升级时不会自动删除掉旧的内核，需要手工删除。因为旧的内核不会再用到了，把旧的删除掉还可以节约/boot的磁盘空间。
按下面步骤进行：
先查看下系统目前所使用的内核并记下：
uname -a
查看系统都安装了哪些内核：
dpkg --get-selections|grep linux
列出来带有image的就是内核文件，类似于linux-image-2.6.24-19-generic 这样是内核的名称。
删除内核：
sudo apt-get remove 内核文件名[![](/assets/images/2008/09/e697a0e6a087e9a298.png)](/uploads/2008/09/e697a0e6a087e9a298.png)
这样就可以实现自动删除内核文件了，还可以释放磁盘空间，一个内核能释放126多M的空间。只要留有最新的内核就好了，旧的完全可以删除掉。

---


