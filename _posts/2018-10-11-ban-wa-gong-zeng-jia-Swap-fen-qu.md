---
title: 搬瓦工增加Swap分区
date: '2018-10-11 00:00:00'
slug: ban-wa-gong-zeng-jia-Swap-fen-qu
categories:
- 网络
tags:
- jekyll
---
29.99年付套餐Swap分区只有130多M， 搭建了wordpress，在搬瓦工kiwivm处查看，经常彪红。
搬瓦工的Swap分区是可以自己调整的，步骤如下：
1. 进入/var目录
# cd /var/
2. 新建个512M的文件块 （数字512可自我更改，一般是内存的一半或相等）
# dd if=/dev/zero of=swapfile bs=1M count=512
3. 创建Swap文件
# /sbin/mkswap swapfile
4. 激活
# /sbin/swapon swapfile
5. 修改权限
chmod 0600 /var/swapfile
6. 将swapfile添加到fstab文件中，并设置开机自动启动
 echo "/var/swapfile swap swap defaults 0 0" >> /etc/fstab
搞定，去后台看看，是不是已经变成600多M了？
![](/assets/images/2018/10/swap.png)

---


