---
title: DreamHost上安装Babel
date: '2007-10-20 00:00:00'
slug: DreamHost-shang-an-zhuang-Babel
categories:
- 网络
tags:
- 网站
- 数据库
- Linux
- 域名
- 服务器
---
一．登陆你的DreamHost后台。
1）新建一个域名(以koryi.com为例)：Domains->Manage Domains->Add New Domain/Sub-Domain，在Specify your web directory一栏这样填写/home/username/koryi.com/htdocs/，因为V2EX Labs 上 Installation 文档中说了如果你是在DreamHost上安装，请在添加 Domain 时指定 DocumentRoot 到 Project Babel 文件夹中的 htdocs 目录。

2）登陆数据库后台，手工导入一个 sql文件 /sql/babel.mysql.sql并执行。

二．在这里下载 Project Babel v0.6，解压缩，修改settings.php如下:

修改
define(’BABEL_PREFIX’, ‘/www/babel’);
为
define(’BABEL_PREFIX’, ‘/home/.jyray/koryi.com’);

define(’BABEL_DB_HOSTNAME’, ‘127.0.0.1′); 你的数据库地址
define(’BABEL_DB_PORT’, 3306); 不用动
define(’BABEL_DB_USERNAME’, ‘XXXXXX’); 你的数据库用户名
define(’BABEL_DB_PASSWORD’, ‘XXXXXX’); 你的数据库密码
define(’BABEL_DB_SCHEMATA’, ‘XXXXXXl’); 你用来跑babel的数据库名称

修改
define(’BABEL_DNS_NAME’, ‘www.v2ex.com’);
define(’BABEL_DNS_DOMAIN’, ‘v2ex.com’);
define(’BABEL_DNS_FEED’, ‘feed.v2ex.com’);
define(’BABEL_FEED_URL’, ‘http://www.v2ex.com/feed/v2ex.rss’);
为
define(’BABEL_DNS_NAME’, ‘www.koryi.com’); 将www.koryi.com换成你的域名
define(’BABEL_DNS_DOMAIN’, ‘www.koryi.com’);
define(’BABEL_DNS_FEED’, ‘www.koryi.com’);
define(’BABEL_FEED_URL’, ‘http://www.koryi.com/feed/v2ex.rss’);
三．编辑 htdocs/core/InstallCore.php 配置初始的分区（Section）及讨论区（Discussion Board）设置。然后从浏览器中访问此文件一次。

InstallCore.php 文件的概念类似于一个批处理文件，不过重复运行不会对系统造成破坏。建议在运行完毕之后，在本地备份这个文件，然后从服务器上删除此文件，否则就是一个可能的性能漏洞。

四．拷贝apachehtaccess.htaccess到htdocs目录下，打开主页这时可能会继续提示一些问题的存在，比如数据库未正确配置或者目录权限问题之类，根据屏幕上的提示逐一修正这些问题。如果不再提示任何错误，那么至此安装基本完成。你可以在这个新网站上注册第一个用户，而这个用户就将成为这个社区里拥有最高权限的管理员。

---


