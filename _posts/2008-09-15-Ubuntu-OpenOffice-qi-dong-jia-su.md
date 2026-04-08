---
title: Ubuntu-OpenOffice启动加速
date: '2008-09-15 00:00:00'
slug: Ubuntu-OpenOffice-qi-dong-jia-su
categories:
- 网络
tags:
- Linux
- 软件
---
OpenOffice 启动速度慢的是一塌糊涂，双击后等了半天还没打开，还以为鼠标没点到呢。安装下列方法修改，瞬间启动：
1. 打开 OpenOffice Writer，在菜单中选择：工具->选项->内存
2. 修改：撤销命令->步数：20
3. 修改：图形缓冲区->用于openoffice：128m，每个对象的内存：20m
4. 取消 Java 选项页中的‘使用 Java 运行环境’
再次重新打开下，感觉启动至少快了1秒。

---


