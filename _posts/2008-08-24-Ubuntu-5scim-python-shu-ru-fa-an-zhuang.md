---
title: Ubuntu-(5)scim-python输入法安装
date: '2008-08-24 00:00:00'
slug: Ubuntu-5scim-python-shu-ru-fa-an-zhuang
categories:
- 科技
tags:
- Google
- Python
- Linux
---
[![](/assets/images/2008/08/e697a0e6a087e9a2981.jpg)](/uploads/2008/08/e697a0e6a087e9a2981.jpg)
scim-python基于scim， 安装后即与scim整合， 整合了搜狗拼音输入法的词库，而且能动态调整词频，用辅助键选词，简单的英文提示。scim-python带了两个输入法：巨蟒拼音输入法和整句输入法。缺点是：因为python的缘故，某些情况下反应比较慢，一般情况下反应速度还是可以。
安装步骤：
http://code.google.com/p/scim-python/downloads/list下载 scim-python源代码包。
执行下列命令:
$ sudo apt-get install scim-dev
$ sudo apt-get install python-enchant
$ sudo apt-get install python-gtk2-dev
$ sudo apt-get install libgtk2.0-dev
$ tar jxvf scim-python-${version}.tar.bz2
$ cd scim-python-${version}
$ ./configure --prefix=/usr
$ make
$ sudo make install

重新登录桌面系统。
设置习惯自己的快捷键：比如左右Ctrl切换中英文，左右shift选词2，3
sudo gedit ~/.scim/config
修改：
/IMEngine/Chewing/ChiEngKey = Control+Control_R+KeyRelease,Control+Control_L+KeyRelease
/IMEngine/Pinyin/ModeSwitchKey = Control+Control_L+KeyRelease,Control+Control_R+KeyRelease

/IMEngine/Table/ModeSwitchKey = Control+Control_L+KeyRelease,Control+Control_R+KeyRelease

重启X，OK。

让scim实现光标跟随：
修改 /etc/X11/xinit/xinput.d/scim 改成这样：
#GTK_IM_MODULE=xim
#QT_IM_MODULE=xim
GTK_IM_MODULE=scim
QT_IM_MODULE=scim

如果出现下列错误：
../libtool: line 1311: g++: command not found
make[2]:  [_scim_la-scim-python.lo] 错误 1
make[2]: Leaving directory `/home/leslie/scim-python-0.1.8/src'
make[1]:  [install-recursive] 错误 1
make[1]: Leaving directory `/home/leslie/scim-python-0.1.8/src'
make:  [install-recursive] 错误 1

安装：sudo apt-get install build-essential gcc make autoconf automake libtool gdb g++

---


