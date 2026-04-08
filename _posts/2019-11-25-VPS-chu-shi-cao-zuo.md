---
title: VPS初始操作
date: '2019-11-25 00:00:00'
slug: VPS-chu-shi-cao-zuo
categories:
- 网络
tags:
- 开源
- Git
- 服务器
---
纪录下VPS重装系统后的初始操作.

1. 安装wget
yum install wget
2. 安装并查看bbr
安装： wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
查看：sysctl net.ipv4.tcp_congestion_control
3. 安装宝塔面板: yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh

---


