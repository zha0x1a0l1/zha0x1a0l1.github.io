---
title: Ubuntu-(6)我的桌面美化
date: '2008-08-25 00:00:00'
slug: Ubuntu-6-wo-de-zhuo-mian-mei-hua
categories:
- 转载
tags:
- Linux
- 服务器
- 软件
---
1.系统更新
访问快[速配置指南(Hardy)版](http://wiki.ubuntu.org.cn/index.php?title=Qref/Hardy&variant=zh-cn)，推荐用户加入Ubuntu.cn99.com更新服务器（江苏省常州市电信，推荐电信用户使用）源，更新速度较快，并加入欧洲官方源和ubuntu-cn源。执行sudo apt-get update。通过“更新管理器”把系统更新到不能再更新为止。这些步骤一定要做完后在进行其他步骤，这样会免去很多麻烦。
2.系统中文化
[![](/assets/images/2008/08/1.jpg)](/uploads/2008/08/1.jpg)
点击菜单中”System-系统管理－Language Support”，在语言支持中找到“汉语”，勾选，应用后，系统会自动下载中文与原包，更新完毕后，重启X，系统据会变成中文。包括Firefox，Openoffice,GIMP等应用程序都会变成中文。系统默认字体为“温泉驿正黑“。
3.字体美化
按照[如何使用圆体来美化](http://wiki.ubuntu.org.cn/index.php?title=%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E5%9C%86%E4%BD%93%E6%9D%A5%E7%BE%8E%E5%8C%96&variant=zh-cn)，将 VeraSansYuanTi 目录移动到字体文件夹并设置字体权限，
sudo mv VeraSansYuanTi /usr/share/fonts/
cd /usr/share/fonts/VeraSansYuanTi
sudo chmod 644 /usr/share/fonts/.ttf ＃这里有些错误
我所使用的方法是：
sudo gnome-open /usr/share/fonts/ 打开字体所在文件夹，将下载的字体文件拷贝到fonts文件夹下，文件夹名字为VeraSansYuanTi。
cd /usr/share/fonts/VeraSansYuanTi
sudo chmod 644 /usr/share/fonts/VeraSansYuanTi/.ttf
注意:在源wiki中设置字体权限的命令有点错误，应设置VeraSansYuanTi目录下的字体权限。
效果图如下：
[![](/assets/images/2008/08/e697a0e6a087e9a2982.jpg)](/uploads/2008/08/e697a0e6a087e9a2982.jpg)
推荐一款强大的字体管理软件：字体管理软件fontmatrix： sudo apt-get install fontmatrix，装上之后安装字体就非常方便了。
4.更改系统主题：
以下内容来源于linuxdesktop的Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)
文章来自：http://linuxdesktop.cn/2008/08/04/glow-theme/在这里转载，非常感谢他推荐的主题。
－－－－－转自[Linux桌面中文网](http://linuxdesktop.cn/) - Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)－－－－－－－－
主题名叫：Glow，来自GNOME-Look.org，与一般的GTK+2的主题不同，它需要另外一个系统并没有自带的GTK+引擎才能使用。因此在安装主题前，需要安装这个名为Aurora的GTK+引擎。
Aurora Gtk Engine可以在这里下载到：
http://www.gnome-look.org/content/show.php/Aurora+Gtk+Engine?content=56438
下载的压缩包里面有两个文件，解压后，其中aurora-1.4.tar.gz是引擎相关的。
[![](/assets/images/2008/08/zaqjpg.jpg)](/uploads/2008/08/zaqjpg.jpg)
将其中的aurora-1.4.tar.gz解包，解压至主目录~/aurora-1.4下。
编译aurora了，确认你已经安装好了相关开发包，如果没有的话，请打开终端执行
sudo apt-get install gnome-core-devel（如果出现无法安装或在安装过程中出现错误，就进行系统更新，把系统更新的不能再更为止。我就遇到过两次不能安装的情况，把系统更新下就好了。）
准备好以后，就开始编译吧！打开你的终端，然后执行下面的指令：
cd ~/aurora-1.4
./configure --prefix=/usr --enable-animation（其中enable-animation这个参数用于启用动画效果，aurora引擎具备一些动画效果）
make
sudo make install（或者你可以用sudo checkinstall来打包）
安装完成后，下载Glow主题。
访问：http://www.gnome-look.org/content/show.php/Glow?content=85996
下载其中的GTK2 Theme（如果你是xfce桌面，选择Xfwm4），这里强烈建议安装Emerald边框，这样才能达到一致的效果。
安装Glow主题和Emerald的边框，到“系统”->“首选择”->“外观”即可安装。安装Emerald，首先保证你sudo apt-get install emerald，然后打开Emerald Theme Manager即可安装。
安装后，根据你自己喜欢的配色，选择喜爱的Glow吧！
[![](/assets/images/2008/08/glow-theme-2.png)](/uploads/2008/08/glow-theme-2.png)
选择Glow Water是比较漂亮的。

－－－－－转自[Linux桌面中文网](http://linuxdesktop.cn/) - Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)－－－－－－－－
5.更改系统图标主题
在gnome-look.oge下载Dropline Neu!
http://www.gnome-look.org/content/show.php/Dropline+Neu!?content=38835
下载后的文件格式为tar.bz2格式，无须解压。
主题安装：在桌面上点右键，选择“更改桌面背景(B)-主题－安装(I)”选择到下载的文件，“打开”，系统就会自动进行安装。然后找到“外观首选现－主题－自定义－图标”，找到安装好的图标单击就可以应用了。
[![](/assets/images/2008/08/1234.jpg)](/uploads/2008/08/1234.jpg)
6.更改桌面背景
这个就不说了，上面的步骤应该看到了更改的选项，这个和windows的差不多。我所使用的背景图片是Distro_Balls_red_by_JackFox05，在[gnome-look](http://www.gnome-look.org/)有的下。
7.更改登录界面GDM
我说使用的是Distro Style Balls，红色的那个，正好与桌面背景想配。可以在http://www.gnome-look.org/content/show.php/Distro+Style+Balls?content=83364下载的到。
不过我已经设置了用户自动登录，这个只有在注销的时候用的到。
[![](/assets/images/2008/08/e697a0e6a087111e9a298.jpg)](/uploads/2008/08/e697a0e6a087111e9a298.jpg)
8.用screenlets添加桌面小部件
sudo apt-get install screenlets
这个可以在桌面上添加一些小部件，如天气预报，RSS Feed，股市行情什么的，进一步美化桌面。安装好后这个软件会自动随系统启动。
[![](/assets/images/2008/08/e697a0e6a087dde9a298.jpg)](/uploads/2008/08/e697a0e6a087dde9a298.jpg)
9.一些其他
可以按照自己的习惯调节设置下面板。

---


