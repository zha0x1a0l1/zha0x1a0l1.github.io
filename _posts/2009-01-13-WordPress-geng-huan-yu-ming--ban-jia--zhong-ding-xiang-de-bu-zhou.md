---
title: WordPress更换域名、搬家、重定向的步骤
date: '2009-01-13 00:00:00'
slug: WordPress-geng-huan-yu-ming--ban-jia--zhong-ding-xiang-de-bu-zhou
categories:
- 转载
tags:
- jekyll
- 网站
- 数据库
- 域名
- 搬家
---
比较详细的步骤，转过来留作备用。
WordPress搬家
WordPress是基于PHP+MySQL数据库的，所以搬家不像使用Access的mdb数据库那样直接拷贝那么简单，再加上更换域名的话，步骤稍微麻烦一点，假如要想更换AAA.com搬家并使用BBB.com域名的话，步骤有以下几步：
1. 在BBB.com建立一个全新的WordPress，并且配置好MySQL的数据库。
2. 拷贝或者移动AAA.com下面的所有文教到BBB.com，并检测文件的正确性。
3.将AAA.com的MySQL数据库导出，然后使用Notepad++之类的文本编辑器打开并替换所有的AAA.com为BBB.com，
保存以后导入到BBB.com的数据库。转到BBB.com的文件架确保wp-cofig.php指向正确的数据库。
4.转到BBB.com的后台，将WordPress的地址更换为BBB.com。
5. 重定向AAA.com到BBB.com，打开AAA.com的网站文件夹根目录，找到或者新建.htaccess，文件内容：
RewriteEngine on
RewriteCond %{HTTP_HOST} bbb.com
RewriteRule ^(.) http://www.bbb.com/$1 [R]
OK。这样访问AAA.com的时候就会马上重定向到BBB.com，更为重要的是访问AAA.com下面的每一个页面也都会重定向到BBB.com的相对页面，例如：访问http://www.AAA.com/news会重定向到http://www.BBB.com/news，这样不仅有利于SEO，而且不会看到404无法访问的页面。

原文来自：[神农贝塔](http://www.sinobeta.com/wordpress-change-domain-moved-redirection.html)

---


