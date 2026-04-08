---
title: 新建或增大交换分区
date: '2009-02-26 00:00:00'
slug: xin-jian-huo-zeng-da-jiao-huan-fen-qu
categories:
- 网络
tags:
- Linux
---
17、Add a swap file or expand existing swap space（新建或增大交换分区）
To create a swap file, you need to first create a dummy file of sufficient size, then format it as a swap file, and finally ensure that Ubuntu uses it at boot-up. The following steps do just that (be extremely careful entering these commands):
（创建扩展分区，先创建一个足够大小的虚拟文件，然后将其格式化为swap 文件格式，最后让系统启动时挂载新建的扩展分区。（此操作有一定危险性，小心操作））
1.	Open a terminal window and create an empty file in the root of the file system using the dd command, as follows (this creates a 1GB file—you should ideally adjust the count= figure to at least match the size of your memory, bearing in mind that there is 1,024MB in a 1GB):
（打开终端，用dd命令在root下创建一个空文件，如下步骤，创建一个1GB大的文件，大小可以根据你内存的大小来调整。1024M=1GB。）
 $ sudo dd if=/dev/zero of=/swapfile bs=1M count=1024
2.	Now we need to format it as a swap file:
（将其格式化成swap文件格式）
 $ sudo mkswap /swapfile
3.The final step is to make Ubuntu mount it at boot, which is done by editing /etc/fstab:
（编辑/etc/fstab文件，使系统在启动时自动挂载新建扩展分区。）
 $ gksu gedit /etc/fstab
Then make a new line at the bottom of the file and add the following:
（在打开的文件最后添加下面一行）
 /swapfile none swap sw 0 0
Once the computer has rebooted, you can test to see if the swapfile is being utilized by typing cat /proc/meminfo|grep Swap.
（重起系统后，可以通过cat /proc/meminfo|grep Swap命令察看扩展分区是否被挂载利用。）
The steps above can also be used to add more swap space to a system that has an existing swap partition.
（这些步骤同样可以用来增加现有扩展分区的大小。）

---


