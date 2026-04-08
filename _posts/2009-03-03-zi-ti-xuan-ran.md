---
title: 字体渲染
date: '2009-03-03 00:00:00'
slug: zi-ti-xuan-ran
categories:
- 网络
tags:
- 软件
---
21、Make fonts look superb（字体渲染）
To activate bytecode hinting, open a terminal window and type the following:
(激活bytecode hinting：)
sudo dpkg-reconfigure fontconfig-config
Using the cursor keys, select Native from the menu and then hit Enter.On the next screen you’ll be asked if you want to activate subpixel rendering. This is good for TFT screens, so make the choice (or just select Automatic). Next you’ll be asked if you want to activate bitmap fonts, which are non-true type fonts good for use at low point levels. There’s no harm in using them, so select yes. The program will quit when it’s finished. Once that’s happened, type the following to write the changes to the system and update files:
(用方向键选择窗口中的Native然后回车，在接下来出现的对话中选择“Always或Automatic”，回车，接下来选择“yes”，回车。完成后窗口自动关闭。然后输入下列命令更新配置文件：)
 sudo dpkg-reconfigure fontconfig
sudo dpkg-reconfigure defoma
Click System ! Quit ! Logout, and then log back in again. The difference should be noticeable immediately. Letters will appear more rounded and the antialiasing will appear better.
(重起X，你会发现字体变得更加圆润，字体看起来更加舒服。)
Bytecode hinting isn’t to everybody’s taste. If you don’t like it, just repeat the steps and enable autohinting again.
(Bytecode hinting渲染并不是每个人都喜欢。你可以重复上面的步骤重新起用autohinting 。)

---


