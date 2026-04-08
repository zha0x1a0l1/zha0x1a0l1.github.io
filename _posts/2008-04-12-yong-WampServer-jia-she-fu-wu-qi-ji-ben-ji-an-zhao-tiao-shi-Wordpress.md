---
title: 用WampServer架设服务器及本机按照调试Wordpress
date: '2008-04-12 00:00:00'
slug: yong-WampServer-jia-she-fu-wu-qi-ji-ben-ji-an-zhao-tiao-shi-Wordpress
categories:
- 网络
tags:
- jekyll
- 数据库
- Linux
- 软件
- 服务器
---
使用WampServer可以简单架设Apache+PHP+MySQL服务器，安装使用起来都非常简单，不需要太多复杂的设置，就可以调试一些流行的PHP+MySQL程序，如Wordpress,Discuz！等。
1.下载安装
下载[WampServer2.0](http://www.wampserver.com/dl.php) 一路Next就可以完成安装，安装完成后启动，在状态栏可以看到WampServer的图标，软件是多国语言版，当然包括中文语言了。
[![](/assets/images/2008/04/gdgs.jpg)](/uploads/2008/04/gdgs.jpg)

2.软件配置
在浏览器里输入http://localhost/或127.0.0.1就可以访问了，自带了一个index.php页面，在tools里包含了phpinfo(),phpmyadmin和sqlitemanager三个工具。打开phpmyadmin会在下方看到提示，root用户没有设置密码，需要先为root帐户设置密码。
[![](/assets/images/2008/04/gggfg.jpg)](/uploads/2008/04/gggfg.jpg)
点击phpmyadmin页面中部的“权限”，可以看到“用户一览”，即root localhost这一行，点击编辑权限图标（1个小人拿个笔的那个），在打开的页面找到“更改密码”，为root用户设置密码，并点击“执行”。
[![](/assets/images/2008/04/6465.jpg)](/uploads/2008/04/6465.jpg)
然后刷新页面，会看到错误提示，这是因为帐户已经设置密码。
[![](/assets/images/2008/04/yfguygjh.jpg)](/uploads/2008/04/yfguygjh.jpg)
到WampServer程序安装目录，在apps目录找到phpmyadmin的目录，打开phpmyadmin目录里面的config.inc.php文件，找到下面这一行：
$cfg['Servers'][$i]['password']       = '';
在等号右面的单引号里面输入刚才设置的密码，重新打开phpmyadmin的页面并刷新，这时候phpmyadmin就可以正常访问了。
这样，一个PHP + MySQL的服务器就架设好了。
3.新建wordpress的数据库
在浏览器输入http://localhost/phpmyadmin/，在“创建一个新数据库”，输入WP，点击“创建”，用来存储wordpress数据。[![](/assets/images/2008/04/dfsfdffs.jpg)](/uploads/2008/04/dfsfdffs.jpg)
4.wordpress的安装
配置wp-config.php文件
> define('DB_NAME', 'wp');    // 输入第三步所建立的数据库的名字
define('DB_USER', 'root');     // 数据库用户名 默认为root
define('DB_PASSWORD', ''); // 输入第二步软件配置中设置的密码
define('DB_HOST', 'localhost');    // 99% chance you won't need to change this value
define('DB_CHARSET', 'utf8');
define('DB_COLLATE', '');
define('DB_COLLATE', '');

下载[wordpress2.5](http://wordpress.org/latest.zip),将解压后的wordpress文件夹拷贝到WampServer的安装目录下的WWW文件夹下，在浏览器输入http://localhost/wordpress/就可以进行安装了。
[![](/assets/images/2008/04/kkkkkn.jpg)](/uploads/2008/04/kkkkkn.jpg)
安装过程与在虚拟机上安装一样，传说中的5步安装法。
安装完成后，在浏览器输入http://localhost/wordpress/，就可以看到本机的wordpress站点了。以后调试和修改就可以都在本机上完成了，等都修改好了在传到服务器上。这样是不是很安全，也很简单啊。
5.其他php程序的安装与上面的步骤一致。Good Luck and Enjoy It!

---


