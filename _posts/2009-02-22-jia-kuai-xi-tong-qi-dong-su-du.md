---
title: 加快系统启动速度
date: '2009-02-22 00:00:00'
slug: jia-kuai-xi-tong-qi-dong-su-du
categories:
- 网络
tags:
- Python
- Linux
---
8、Optimize startup for faster boot Times（加快系统启动速度）
There are four things you can do to reduce delays and generally speed-up startup:
(四种方法来减少系统启动时间)
• Reduce or eliminate the boot menu countdown;
(减少或取消boot menu 的等待时间)
• Make boot runtime scripts start in parallel;
(并行运行启动脚本文件)
• Build a read-ahead profile personalized to your PC;
• Reduce the number of GNOME startup programs.
(减少随机启动程序)
Reducing the boot menu delay
Start by opening the boot menu configuration file in Gedit:
(编辑boot menu configuration 文件：)
 gksu gedit /boot/grub/menu.lst
search for the line that reads timeout 10 and change the 10 to read either 1, for a one second countdown, or 0, to disable the boot menu completely.
(找到reads timeout 10 这一行，将10改为1（现实启动菜单1秒）或0（不显示启动菜单），保存并退出。)
Run boot-time scripts in parallel
open the necessary configuration file in Gedit:
(编辑configuration 文件：)
 gksu gedit /etc/init.d/rc
Look for the line that reads CONCURRENCY=none and change it so it reads CONCURRENCY=shell. Then save the file and reboot your computer.
(找到CONCURRENCY=none行，将none改为shell，保存后推出。)
Build a readahead profile personalized to your computer
Reboot Ubuntu and, at the boot menu, ensure the usual Ubuntu entry is highlighted. Then hit e . This will let you temporarily edit the boot menu entry. Use the cursor keys to move the highlight down to the second line that beings kernel and hit e again. Use the right arrow key to move to the end of the line and, after the words quiet and splash, add the word profile. Then hit Enter and then b to boot your computer. Note that the first boot will be slow because the readahead cache will have to be rebuilt.
In subsequent boots, however, you should see speed improvements.
Trimming the GNOME startup programs
use the GNOME Sessions program (System ! Preferences ! Sessions). Ensure the Startup Programs tab is selected and then look through the list for items you might want to prune.
依次打开“系统-首选项-会话”，取消掉你不会用到或者不需要随机启动的程序。

---


