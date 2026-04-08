---
title: Ubuntu-LiHeiPro字体推荐
date: '2008-09-06 00:00:00'
slug: Ubuntu-LiHeiPro-zi-ti-tui-jian
categories:
- 科技
tags:
- Apple
- Linux
- 软件
---
LiHeiPro字体看起来很舒服，中文字体显示很好
安装方法：
1、在这里[下载LiHerPro字体](http://www.rayfile.com/files/e6666742-7bcf-11dd-adbd-0014221b798a/)
2、将字体拷贝到/usr/share/fonts下，建立文件夹名为apple
3、修改字体权限
sudo chmod 755 /usr/share/fonts/apple/LiHeiPro.ttf
4、建立字体缓存
cd /usr/share/fonts/apple/
sudo mkfontscale
sudo mkfontdir
然后就可以设置系统字体了，看起来是不是很舒服，很有apple的感觉？

---


