---
title: Win7下全新安装新版本Win7
date: '2009-06-26 00:00:00'
slug: Win7-xia-quan-xin-an-zhuang-xin-ban-ben-Win7
categories:
- 科技
tags:
- 加密货币
- 工作
- 科技
---
说明：其实安装步骤和用光盘安装相似，只是要想办法来运行硬盘上的安装程序，这样省去了刻盘的麻烦。
目的：在现有Win7下硬盘全新安装Win7。
前提：电脑中已有Win7系统。
准备工作：
1、下在最新镜像文件并解压到到非C：盘（如D:，E:盘），并将文件夹重命名为win7。
2、C：盘容量至少为15G，推荐20G大小(安装过程可调整分区大小)。
安装步骤：
1、重新启动系统，按住F8，选择“修复计算机”，在“Windows 正在加载系统后”，在“System Recovery Options”中选择好Language何keyboard input method，按Next，然后选择User Name ,输入password，按Next。
2、然后在“System Recovery Options”中选择最后一项“Command Prompt”，输入d：回车，cd win7，cd sources，setup.exe启动安装程序。
选择好“语言、时区、键盘类型”,下一步。然后在“Which type of installation do you want ?”中选择最下面的“自定义（高级）”。
3、然后就可以看到分区信息了，选择“驱动器选项（高级）”，这里可以对硬盘进行删除，新建等操作。将原来的C：盘删除或格式化。然后把系统按转到原来的C：盘空间上。
分区完成后，会有个100M的系统保留空间（这个是做什么的？交换分区？
4、选择到要安装系统的分区所在。下一步，系统开始安装。无需多余操作，大概30分钟左右系统安装完成。

---


