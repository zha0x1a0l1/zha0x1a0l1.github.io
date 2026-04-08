---
title: Ubuntu-Firefox中Flash播放器乱码问题
date: '2008-08-17 00:00:00'
slug: Ubuntu-Firefox-zhong-Flash-bo-fang-qi-luan-ma-wen-ti
categories:
- 科技
tags:
- 音乐
- Google
- Linux
---
![](/assets/images/2008/08/ubuntulogo.png)如下两步：

（1）备份49-sansserif.conf这个字体配置文件
 sudo cp /etc/fonts/conf.d/49-sansserif.conf /etc/fonts/conf.d/49-sansserif.conf.bak
（2）删除49-sansserif.conf文件做完后重启firefox就可以了。
 sudo rm /etc/fonts/conf.d/49-sansserif.conf
重新启动，在打开就好了，[Goolge音乐搜索](http://www.google.cn/music)中个歌曲名字就不是乱码了。

---


