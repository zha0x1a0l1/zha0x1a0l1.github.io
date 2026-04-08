---
title: 博客更换域名时出现的错误
date: '2009-02-04 00:00:00'
slug: bo-ke-geng-huan-yu-ming-shi-chu-xian-de-cuo-wu
categories:
- 网络
tags:
- jekyll
- 网站
- 域名
- 数据库
---
上次博客[更换域名](http://blog.zhaoxiao.li/2009/01/18/how-to-change-wordpress-blog-url/)时，数据库全部替换后，博客顶部出现了类似
	- [b]Warning[/b]: Invalid argument supplied for foreach() in [b]/home/blog.zhaoxiao.li/domains/3dian9.host9.meyu.net/public_html/wp-includes/widgets.php[/b] on line [b]676[/b]

的错误，一直显示在页面顶部，FTP删掉所有插件也都不惯用，并且不能登录到博客后台。
解决方法：
登录到你的博客数据库，选择wp-options条目并清空，这样重新打开你的博客，博客重新安装，然后在去后台重新激活所有插件，再逐一配置一下就好了。

---


