---
title: 博客迁移到搬瓦工VPS
date: '2018-10-07 00:00:00'
slug: bo-ke-qian-yi-dao-ban-wa-gong-VPS
categories:
- 网络
tags:
- jekyll
- 网站
- 数据库
- Linux
- 软件
---
关于搬瓦工：
1. 现在有19.99的年付套餐，如果不在意速度的，可撸。 （本人江苏电信200M，感觉速度不行）
2. 建议购买29.99 CN2 的年付套餐， [连接直达](https://bwh1.net/cart.php?gid=1)，使用优惠码 BWH26FXH3HIQ可便宜6%。每年多10块，但真是质的飞跃，强烈推荐。（本站目前就是。）
Wordpress建站：（小记）
1. 先重装系统， 推荐： Centos 7 x86_64 bbr， 安装完成后会收到root密码邮件。
2. SSH 连接软件推荐： Xshell 5 （需要IP, 连接密码，端口默认 22）
3. 安装宝塔面板： yum install -y wget && wget -O install.sh http://download.bt.cn/install/install.sh && sh install.sh
1） 当出现下图的时候，说明安装成功，备份好BT - Panel, Username, password等信息。
[![](/assets/images/2018/10/1-300x186.png)](/uploads/2018/10/1.png)

2） 用刚刚记录的信息登录
[![](/assets/images/2018/10/2-300x254.png)](/uploads/2018/10/2.png)

3）首次进入后，一键安装LNMP，等一会。
[![](/assets/images/2018/10/3-300x191.png)](/uploads/2018/10/3.png)

4）安装中
[![](/assets/images/2018/10/4-300x281.png)](/uploads/2018/10/4.png)

5）在软件处选择 宝塔一键部署源码1.1，找到wordpress， 就可以愉快的安装了。
[![](/assets/images/2018/10/6-300x163.png)](/uploads/2018/10/6.png)

4. 宝塔面板， 可进行文件上传，数据库导入等操作。 其余菜单可自我摸索。

---


