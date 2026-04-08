---
title: 卸载Ubuntu
date: '2009-04-17 00:00:00'
slug: xie-zai-Ubuntu
categories:
- 科技
tags:
- 科技
- Linux
- 软件
---
卸载之前请务必做好资料备份，防止万一发生意外。主要讲述Windows 与 Ubuntu组成的双启动系统中，卸载Ubuntu的方法。
目的：完全删除Ubuntu系统，保留windows，并将ubuntu分区转化为windows分区。
1、用 Ubuntu安装光盘启动电脑，在刚开始出现的启动菜单中选在“试用Ubuntu而不改变计算机中的任何内容(T)”。系统启动后，依次打开“System-系统管理-Partition Editor”。
2、找到ubuntu的交换分区,类似于linux-swap（有两把钥匙的图标，Filesystem为深红色小方框），右键点击，在弹出的菜单中选择“Swpoff”。
3、找到ubuntu分区，通常文件格式为ext3(非Fat,Fat32或NTFS分区格式，Filesystem为深蓝色小方框)，右键点击，在弹出的菜单中选择“Delete”，同样的方法也删调linux-swap分区。确保所有ubuntu分区都已被删除。然后点击中间的绿色对勾图标(Apply),在弹出的对话框中选Apply，删除完成后close关掉。
4、右击与刚刚删掉的Linux分区相邻的Windows分区（通常文件格式为Fat,Fat32或NTFS的分区），选择“Resize/Move”， 在出现的对话框中， 拖动滚动条右边的黑色小三角图标到最大位置（直至Free Space Following中的数字变为0），点“Resize/Move”， 然后点击中间的绿色对勾图标(Apply),在弹出的对话框中选Apply。开始将删除掉的linux分区与Windows分区合并。完成后close关闭。
5、将windows安装光盘放入光驱启动电脑，光盘内容加载完成后，选择到原来系统所在的硬盘分区，按回车键进入，然后按Esc取消，按两次F3键退出，重起后就能正常进入Windows了。

---


