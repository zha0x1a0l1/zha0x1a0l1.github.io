---
title: 安装KDE桌面环境
date: '2009-04-06 00:00:00'
slug: an-zhuang-KDE-zhuo-mian-huan-jing
categories:
- 网络
tags:
- Google
- Linux
- 软件
---
玩惯了Gome, 装个KDE来玩玩。安装起来比较简单。

sudo apt-get install kubuntu-desktop
 （安装kubuntu桌面环境，会附带安装一些KDE下的优秀软件，大概要下载200多M的文件）

sudo apt-get install language-pack-kde-zh language-pack-kde-zh-base language-pack-zh language-pack-zh-base language-support-zh
（安装中文语言包）
安装完成后，登出系统，在登录的时候选择“会话－KDE”，进入就好了。
卸载：

sudo apt-get remove kubuntu-desktop & sudo apt-get --purge remove kdelibs4c2a & sudo apt-get --purge remove kdelibs4 libart
（卸载的比较干净）
还有几个与KDE相关的东东没有被卸载，在新立得里搜索KDE，把与KDE桌面环境相关的都卸掉就好了。
最后在清理下系统，sudo apt-get autoremove 。

---


