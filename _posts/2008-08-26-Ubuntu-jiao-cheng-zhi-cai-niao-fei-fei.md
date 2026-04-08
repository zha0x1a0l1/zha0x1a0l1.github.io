---
title: Ubuntu教程之菜鸟飞飞
date: '2008-08-26 00:00:00'
slug: Ubuntu-jiao-cheng-zhi-cai-niao-fei-fei
categories:
- 转载
tags:
- jekyll
- 网站
- Python
- Linux
- 软件
---
Ubuntu教程之菜鸟飞飞
作者：Happy  Mail:admin@blog.zhaoxiao.li 网站：blog.zhaoxiao.li
(欢迎转载，版权没有，违者不究)
一.安装与卸载
安装-四种方法：
（1）直接在光驱放入安装光盘，用光盘启动电脑，然后选择Try Ubuntu without any change to your computer ,这样就可以直接进入Ubuntu进行体验。可以测试电脑硬件是否支持，能不能良好的运行Ubuntu。
这种方法只是用来体验用的，有点像Windows下的WinPE。
（2）在Windows系统下，在光驱放入刻录好的光盘或用虚拟光驱加载下载的镜像文件，双击打开光驱，在弹出的对话框选择第二个选项“在Windows中安装（像其他软件一样安装和卸载Ubuntu，而不需要单独的分区。您将可以在启动时选择进入Windows或Ubuntu。在这种模式下，休眠功能不可用，并且磁盘性能会略有降低。）”，然后在弹出的对话框中选择好要安装的驱动器，安装大小，语言，用户名，和设置好密码，就可以了，点击安装，系统会自动进行安装直到安装完成。
这种方法的好处是无需对电脑硬盘进行重新分割，不会破坏原有分区。就像安装Windows下的软件一样，安装方法简单方便。装完之后构成Windows与Ubunt双系统。但注意，在程序安装到82%的时候，会出现“正在进行镜像扫描”，这是系统在扫描服务器上的镜像文件，下在需要的语言包和相应的更新。如果你的网速不够快，建议拔掉网线进行，要不然就需要等很久很久。
（3）常规安装。在光驱放入Ubuntu的安装光盘，用光盘启动系统，选择好要安装的系统语言，然后选择“安装Ubuntu（I）”，进行安装。等待。，，前进，前进，前进。到“预备硬盘空间”出进行系统分区，推荐选择第三项，“手动”，因为原来的XP我还需要，前进，在这里进行分区。把原来在Windows中闲置的空间进行分区，Ubuntu分区空间最好放在硬盘的最后面，离Windows越远越好些。我是这样分区的：
/        15－20G
/home    最大空间
/swap    2048M
/boot    128 M
然后是前进，等待。直到系统安装完成。完成后，光驱会自动弹出。
这种是常规安装方法。要想真正使用，推荐这种安装方法。装完之后构成Windows与Ubunt双系统。但注意，在程序安装到82%的时候，会出现“正在进行镜像扫描”，这是系统在扫描服务器上的镜像文件，下在需要的语言包和相应的更新。如果你的网速不够快，建议拔掉网线进行，要不然就需要等很久很久。
（4）格掉所有的硬盘，只安装一个Ubuntu系统。安装步骤方法如上（3）中所述，只是在分区时选择“向导-使用整个磁盘”进行分区就可以了。
这样安装，电脑中就只有一个Ubuntu系统系统了，而且使用了所有的硬盘空间，不推荐还对Windows系统有依赖的朋友安装。毕竟，目前Linux下还不能使用支付宝，网络银行，也不能打暗黑，不能打魔兽，连跑跑卡丁车都不能跑。
卸载－对应上述四种安装：
（1）无需卸载，只要把光盘从光驱里抽出来就好了。简单。
（2）进入Windows系统，找到你所安装Ubuntu的硬盘分区（第二种安装方法是能在Windows下看到你用来安装Ubuntu系统的硬盘分区的，因为没有对硬盘空间进行任何改变，原来硬盘是什么格式，现在还是什么格式）。在硬盘分区上点右键，选择“格式化（A）…”,勾选“快速格式化”就好了，这样Ubuntu就完全删除了。然后右击“我的电脑”－“属性”－“高级”，启动和故障恢复中的“设置”－“编辑”，把文本中的Ubuntu删除，保存推出就好了。这样Ubuntu系统就完全删除了，一点痕迹都没留下。
注：虽然在Ubuntu的安装目录下和控制面板的“添加或删除程序中”有“Uninstall”的选项，但却无任何功能，这还只是形式上的，无论在XP或Vista中都不管用。
（3）找个能启动的带有硬盘分区魔术师光盘，启动电脑，把你所分的Ubuntu分区都给删除掉，就好了。重起后，进不了Windows了，晕吧，不过没关系。再找个Windows的安装盘（那种GHOST的可不兴哦），启动电脑，进行正常的安装，等到出现选择硬盘分区的时候，不选择，直接退出就好了。重起电脑后，呵呵，能进Windows了。
（4）这个没什么好说的，直接想办法把所有盘都格了就好了。然后想装什么就装什么吧。
二.初体验
按下Power键，开机喽。哦？怎么出了这么多的启动选项，仔细一看，原来的Windows系统还在，选择到最后一个启动选项，看看原来的系统还在不在？回车，顺利进入了原来的Windows系统，简单操作下，还和原来一样呢？高兴ing…重新启动，进入Ubuntu体验下。就选第一个启动选项好了，看着那漂亮的Logo,那漂亮的Ubuntu字体，还有那漂亮又不失个性的滚动条，看着这一切，都是那么令人兴奋，果然这里还有另一片天地呢。连登陆界面都个性的不行，怎么看着这个就格外舒服呢？
输入用户名和密码，进入到了桌面。这里果然别有洞天阿。哦？怎么有两个“任务栏”呢？上面一个，下面还有一个呢？呜呼，怪哉。再仔细一看，哦？安装的时候明明是选的中文阿？怎么上面却是Application,Places,System的英文字母呢？再用鼠标点点，原来这些都能弹出菜单呢，这些都是中文。哦，原来这个系统是中英夹杂的。
把每个“东东”都点一点，都看看是做什么用的吧，至少也要知道怎么操作撒。
经过一番的折腾，乱点，发现如下问题：
鼠标右键没有刷新选项，习惯在Windows下点刷新的现在还真不习惯。难道这个系统不用刷新？
桌面图标排列方式也只有“Clean Up by Name”
垃圾桶哪里去了？找了很久之后才发现，原来右下角的那个好像就是。
左下角的这个又是什么东东？点了好几下也没任何反应。
怎么好多软件都是英文的呢？难道没完全汉化？
这个系统的中文字体怎么这么难看，果然是老外的东西，审美观和我们不一样。
打开Places的计算机，能看到Windows下的分区，还能读取里面的文档，不错，赶紧      把里面的美女图片拷过来，给桌面也换张壁纸养养眼。
那个Filesystem盘应该是放Ubuntu的地方，不过怎么只有一个盘呢？明明记得分区的时候我分了四个“盘”呢啊？
打开一看，里面好多文件夹，也不知道是干什么的，不管它了。
哦？桌面出现了一个硬盘，“21GB Media”,这个是什么东西，刚才桌面上好像没有这个图标呢？
该摸的地方也摸的差不多了，基本也知道每个东东是干什么用的了。今天就研究到这里吧，好多困惑呢，这个系统果然很另类。看来要学习的东西还有很多很多阿。
上面的“任务栏”有Firefox的图标，这个偶知道，是用来上网的，还是上会网吧，今天的新闻还没看呢。
打开BaiDu,想搜索下“Ubuntu论坛“，按了半天的Ctrl+Blackspace,怎么就是出不来输入法呢？难道这个系统没有中文输入法，那那些大虾是怎么用的，也需要装个吧，不过偶也知道，搜狗输入法在这个系统下面肯定是装不上的。去论坛研究研究吧。
虽然不能输中文，不过偶知道在百度里输入luntan,回车，百度就会问你“你要找的是不是：论坛”咱就复制下，在搜索。发现两个好地方：
http://forum.ubuntu.org.cn
http://wiki.bubuntu.org.cn
果然，这里有很多内容耶，泡论坛与wiki中......
三.快速配置
关于这点，具体请看
http://wiki.ubuntu.org.cn/Qref/Hardy  这里已经说明的很详细了。
只有几点说明，给从没有接触过Linux系统的朋友看：
（1）终端：依次打开 Application-附件-中断。是个输命令的地方，有点像Windows下的CMD,命令提示符。
（2）在终端里不支持Ctrl+V粘贴命令，只能用右键Paste。别的时候是支持的。
（3）在“我们推荐的源”里注意选择到正确的源。选择Hardy(8.04)版本的。
（4）桌面右上角的那个中间带感叹号的箭头出现，就是在提示你系统有新的更新了。
只要按照Wiki里面的步骤一步一步进行就好了，更新是个漫长的等待过程，尤其是网速不快的时候
四.细说分区
一些疑问：
我可不可以把硬盘分几个区，就像Windows中的那样，分成C:,D:,E:…，这样把系统安装在C盘，其余的资料备份到其他硬盘，这样在重装系统的时候只要把C盘给格了就可以了？
Ubuntu(Linux)的文件结构：
Ubuntu的文件结构是树形结构，最顶层是根分区 / ，在跟分区下面建立了很多文件夹，来存放系统所需文件。如/bin, /boot ,/home , /tmp….给人的感觉（已经习惯了Windows的用户来说）就像整个一个硬盘没有分区，只是建立了许多文件夹来存放不同的文件。那要是重装系统还不都得把文件删除了？
其实：
是可以把如/home目录，/tmp 目录，/boot 目录及任何你想要的目录单独分出来的，即使这样分出来，但在系统下，这些分区还是存在于根目录/ 下，还是像在根目录 / 下建了些文件夹。其实不然，这些单独分出来的分区，确实已经是独立存在的了，只是不同于Windows中的表现形式罢了，这就是树形结构的特点。慢慢的就会习惯了。
推荐分区方法：
/boot  分个128M足以
/swap  通常是内存的两倍（那时在128M内存时的分法），现在动辄就是2G内存了，分大了也没什么用，推荐分个512M就好了，要是不放心就分1G,我分的是2G，不过好像系统从来没用到过。
/home 要是你文件（资料，音乐，电影）较多，这个就多分点吧，所有的资料都放到这里，重新装系统的时候才不会丢失。
/      这个是根分区，网上说有个10到20G就足以了，这里存放了一些系统所需要的文件，至于到底需要多大卫最好，我还没研究过，问问百度吧。不过肯定够用就好了，分大了也是浪费。
至于文件格式，默认的都是ext3，最新的文件格式，是默认的，默认的总是最好的。
这种分区的好处：
要是不小心把系统搞瘫痪了，重装系统的时候，就可以把根分区 / , /boot 分区， /swap 都格掉或删除，只要不动/home分区，你的资料及系统配置就还在保留。而不同担心资料丢失了。有一点要注意的地方，装系统的时候一定要选择到你原来的/home分区并挂起，这样系统才知道你还是要用原来的/home分区的。要不然，系统可不认的哦。
五．常用命令收集与整理
• 清理无用的包： sudo apt-get clean && sudo apt-get autoclean
•修复安装"-f = --fix-missing"： sudo apt-get -f install
•搜索包：apt-cache search package
•安装硬盘温度监控： sudo apt-get install hddtemp
•查看硬件信息： sudo lshw
•把ubuntu删除后不能启动window用启动盘进入DOS，执行 fdisk /mbr
•建立拨号： sudo pppoeconf
•StarDict辞典： http://stardict.sourceforge.net/Dictionaries_zh_CN.php
•以Root权限打开文件夹（右键菜单）：sudo apt-get install nautilus-gksu
•终端加到右键菜单：sudo apt-get install nautilus-open-terminal
•修复安装：sudo apt-get -f install
•监视温度：sudo apt-get install sensors-applet
•Conky配置文件：zcat /usr/share/doc/conky/examples/conky.conf.gz > ~/.conkyrc
•Mplayer：http://wiki.ubuntu.org.cn/MPlayer
•Gstreamer 多媒体引擎解码器：sudo apt-get install gstreamer0.10-ffmpeg gstreamer0.10-pitfdll gstreamer0.10-plugins-bad gstreamer0.10-plugins-bad-multiverse gstreamer0.10-plugins-ugly gstreamer0.10-plugi
•Xine多媒体引擎解码器：sudo apt-get install libxine1-ffmpeg libxine1-all-plugins libxine1-plugins w32codecs gcc-3.3-base libstdc++5
•安装Firefox的Flash插件： sudo apt-get install flashplugin-nonfree
•安装Emerald Theme Manager：sudo apt-get install emerald
•安装编译开发包：sudo apt-get install gnome-core-devel
•Ubuntu8.04并不像Windows可以对任何文件（文件夹）进行读、写、创建、拷贝和删除。用下面的命令打开fonts:：sudo gnome-open /usr/share/fonts/
更多内容在：http://blog.zhaoxiao.li/ubuntu
六．升级后多出的启动菜单
在官方网站下载Ubuntu 8.04桌面版的Linux内核是2.6.24-19，安装好后把系统升级到最新，内核变成了2.6.24-20。这是在开机的选择启动项里就多出了两个启动选择，如下图：
![](/assets/images/2008/08/1111.jpg)
而在通常情况下，我们就没必要再进入旧的内核系统了，我们把不需要的两个启动选择项删掉。
备份menu.lst，防止出错:
•sudo cp /boot/grub/menu.lst /boot/grub/menu.lst.backup
编辑menu.lst:
•sudo gedit /boot/grub/menu.lst
找到如下文字：
## ## End Default Options ##
title Ubuntu 8.04.1, kernel 2.6.24-20-generic
root (hd0,8)
kernel /boot/vmlinuz-2.6.24-20-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro quiet splash locale=zh_CN
initrd /boot/initrd.img-2.6.24-20-generic
quiet
title Ubuntu 8.04.1, kernel 2.6.24-20-generic (recovery mode)
root (hd0,8)
kernel /boot/vmlinuz-2.6.24-20-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro single
initrd /boot/initrd.img-2.6.24-20-generic
title Ubuntu 8.04.1, kernel 2.6.24-19-generic
root (hd0,8)
kernel /boot/vmlinuz-2.6.24-19-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro quiet splash locale=zh_CN
initrd /boot/initrd.img-2.6.24-19-generic
quiet
title Ubuntu 8.04.1, kernel 2.6.24-19-generic (recovery mode)
root (hd0,8)
kernel /boot/vmlinuz-2.6.24-19-generic root=UUID=d647ec45-7f6d-48b7-87c4-631016eaabf8 ro single
initrd /boot/initrd.img-2.6.24-19-generic
title Ubuntu 8.04.1, memtest86+
root (hd0,8)
kernel /boot/memtest86+.bin
quiet
### END DEBIAN AUTOMAGIC KERNELS LIST
把上面画线的文字删除，保存退出后就好了。
PS:推荐一个系统启动管理工具，qgrubeditor，通过这个管理起来就方便多了。
安装：sudo apt-get install qgrubeditor
七. Firefox中Flash播放器乱码问题
（1）备份49-sansserif.conf这个字体配置文件
•sudo cp /etc/fonts/conf.d/49-sansserif.conf /etc/fonts/conf.d/49-sansserif.conf.bak
（2）删除49-sansserif.conf文件做完后重启firefox就可以了。
•sudo rm /etc/fonts/conf.d/49-sansserif.conf
八. 安装温度监视器
![](/assets/images/2008/08/e697a0e6a087e9a298.jpg)
(1)安装Hardware Sensors Monitor:
•sudo apt-get install sensors-applet
在面板上你想要插入的地方点右键，选择“添加到面板“，找到
![](/assets/images/2008/08/asf.jpg)
点击“添加”这时在面板上就能显示出CPU的温度了。
（2）安装硬盘温度监控：
•sudo apt-get install hddtemp
然后在刚刚新建立的CPU温度的图标处点右键，选择“Preference“，然后选择”Sensors”,找到“hddtemp”选项并展开，将其Enabled选项够选。
![](/assets/images/2008/08/123456.png)
这样，就能看到硬盘的温度了。
九.scim-python输入法安装
![](/assets/images/2008/08/e697a0e6a087e9a2981.jpg)
scim-python基于scim， 安装后即与scim整合， 整合了搜狗拼音输入法的词库，而且能动态调整词频，用辅助键选词，简单的英文提示。scim-python带了两个输入法：巨蟒拼音输入法和整句输入法。 缺点是：因为python的缘故，某些情况下反应比较慢，一般情况下反应速度还是可以。
安装步骤：
http://code.google.com/p/scim-python/downloads/list下载 scim-python源代码包。
执行下列命令:
$ sudo apt-get install scim-dev
$ sudo apt-get install python-enchant
$ sudo apt-get install python-gtk2-dev
$ sudo apt-get install libgtk2.0-dev
$ tar jxvf scim-python-${version}.tar.bz2
$ cd scim-python-${version}
$ ./configure –prefix=/usr
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
make[2]: Leaving directory `/home/leslie/scim-python-0.1.8/src’
make[1]:  [install-recursive] 错误 1
make[1]: Leaving directory `/home/leslie/scim-python-0.1.8/src’
make:  [install-recursive] 错误 1
安装：sudo apt-get install build-essential gcc make autoconf automake libtool gdb g++
十.我的桌面美化
1.系统更新
访问快[速配置指南(Hardy)版](http://wiki.ubuntu.org.cn/index.php?title=Qref/Hardy&variant=zh-cn)，推荐用户加入Ubuntu.cn99.com更新服务器（江苏省常州市电信，推荐电信用户使用）源，更新速度较快，并加入欧洲官方源和ubuntu-cn源。执行sudo apt-get update。通过“更新管理器”把系统更新到不能再更新为止。这些步骤一定要做完后在进行其他步骤，这样会免去很多麻烦。
2.系统中文化
![](/assets/images/2008/08/1.jpg)
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
注意，在源wiki中设置字体权限的命令有点错误，应设置VeraSansYuanTi目录下的字体权限。
效果图如下：
![](/assets/images/2008/08/e697a0e6a087e9a2982.jpg)
推荐一款强大的字体管理软件：字体管理软件fontmatrix： sudo apt-get install fontmatrix，装上之后安装字体就非常方便了。
4.更改系统主题：
以下内容来源于linuxdesktop的Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)
文章来自：http://linuxdesktop.cn/2008/08/04/glow-theme/在这里转载，非常感谢他推荐的主题。
－－－－－转自[Linux桌面中文网](http://linuxdesktop.cn/) - Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)－－－－－－－－
主题名叫：Glow，来自GNOME-Look.org，与一般的GTK+2的主题不同，它需要另外一个系统并没有自带的GTK+引擎才能使用。因此在安装主题前，需要安装这个名为Aurora的GTK+引擎。
Aurora Gtk Engine可以在这里下载到：
http://www.gnome-look.org/content/show.php/Aurora+Gtk+Engine?content=56438
下载的压缩包里面有两个文件，解压后，其中aurora-1.4.tar.gz是引擎相关的。
![](/assets/images/2008/08/zaqjpg.jpg)
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
安装Glow主题和Emerald的边框，到“系统”->“首选择”->“外观”即可安装。安装Emerald，首先保证你sudo apt-get install emerald，然后打开Emerald ThemeManager即可安装。
安装后，根据你自己喜欢的配色，选择喜爱的Glow吧！
![](/assets/images/2008/08/glow-theme-2.png)
选择Glow Water是比较漂亮的。
－－－－－－－－转自[Linux桌面中文网](http://linuxdesktop.cn/) – Glow：[非常漂亮的GNOME主题](http://linuxdesktop.cn/2008/08/04/glow-theme/)－－－－－－
5.更改系统图标主题
在gnome-look.oge下载Dropline Neu!
http://www.gnome-look.org/content/show.php/Dropline+Neu!?content=38835
下载后的文件格式为tar.bz2格式，无须解压。
主题安装：在桌面上点右键，选择“更改桌面背景(B)-主题－安装(I)”选择到下载的文件，“打开”，系统就会自动进行安装。然后找到“外观首选现－主题－自定义－图标”，找到安装好的图标单击就可以应用了。
![](/assets/images/2008/08/1234.jpg)
6.更改桌面背景
这个就不说了，上面的步骤应该看到了更改的选项，这个和windows的差不多。我所使用的背景图片是Distro_Balls_red_by_JackFox05，在[gnome-look](http://www.gnome-look.org/)有的下。
7.更改登录界面GDM
我说使用的是Distro Style Balls，红色的那个，正好与桌面背景想配。可以在http://www.gnome-look.org/content/show.php/Distro+Style+Balls?content=83364下载的到。
不过我已经设置了用户自动登录，这个只有在注销的时候用的到。
![](/assets/images/2008/08/e697a0e6a087111e9a298.jpg)
8.用screenlets添加桌面小部件
sudo apt-get install screenlets
这个可以在桌面上添加一些小部件，如天气预报，RSS Feed，股市行情什么的，进一步美化桌面。安装好后这个软件会自动随系统启动。
![](/assets/images/2008/08/e697a0e6a087dde9a298.jpg)
9.一些其他
可以按照自己的习惯调节设置下面板。
十一．后记
写到这，差不多也有1万字了，不打算写下去了。以后，相关的Ubuntu文章会主要发到我的Blog上。说不定，哪天实在是空的很了或者兴趣来的时候我会整理成这种形势。不过那，也许那是在一段时间之后了。我是一个Ubuntu的初学者，也是一个爱好者，在以后日子里，Ubuntu会是我的主要OS，我会一直使用下去。在我所使用的过程中，肯定会有在你使用过程中所遇到的问题，要是你没有好地解决方法，就来我的Blog看看吧，说不定在这里你会有意外的收获。当然，如果你有好的技巧，新的软件，也欢迎发Mail给我。
推荐一个人用Ubuntu真的很难，即使他是计算机专业的，使用电脑已好多年。而我，又不是Ubuntu的传教士。
在现实中，像我这样的人真的很少，在这么多年中，只有我宿舍的一个兄弟（孙）有着与我同样的爱好。而我周围的99.999%的人，也许等到他们老去都不知道原来除了Windows还有像Ubuntu这样的Linux系统存在，就像他们永远也不知道除了IE可以浏览网页，Firefox也有同样的功能，而且比IE更好些。每个人都有自己的兴趣吧。
我的联系方式：admin@blog.zhaoxiao.li  欢迎发mail给我。也欢迎访问我的blog:http://blog.zhaoxiao.li
＃版权没有，欢迎转载，违者不究＃

---------------------------------下载地址在这里呢----------------------------------
Ubuntu之菜鸟飞飞.doc下载：[http://www.rayfile.com/files/6295a130-7361-11dd-8b9d-0014221b798a/](http://www.rayfile.com/files/6295a130-7361-11dd-8b9d-0014221b798a/)
Ubuntu之菜鸟飞飞.odt下载：[http://www.rayfile.com/files/629c5668-7361-11dd-a346-0014221b798a/](http://www.rayfile.com/files/629c5668-7361-11dd-a346-0014221b798a/)
Ubuntu之菜鸟飞飞.pdf下载：[http://www.rayfile.com/files/62a70947-7361-11dd-b836-0014221b798a/](http://www.rayfile.com/files/62a70947-7361-11dd-b836-0014221b798a/)

---


