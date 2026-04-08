---
title: 如何更改wordpress博客域名
date: '2009-01-18 00:00:00'
slug: ru-he-geng-gai-wordpress-bo-ke-yu-ming
categories:
- 网络
tags:
- jekyll
- 工作
- 网站
- 数据库
- 域名
---
Hello Everyone! Welcome to visit!是不是走错了，没。本博更新的全新的域名，blog.zhaoxiao.li(三点九，简单好记，Web2.0)，目前旧域名仍然有效。到今年6月完全停止旧域名使用。做友情链接的朋友请使用新域名：三点九  http://blog.zhaoxiao.li。
下面记录下本次操作过程：
将新域名解析到主机空间。因为只是更改域名，不涉及到博客搬家的过程，等域名解析做好了，就可以开始操作了。
注意注意注意：操作之前一定要做好备份工作，要不如，哭都来不及。胆大，心细。
注意：修改之前最好去博客后台停用所有插件。
还要注意：下面的标点要都要用英文半角，如果你直接copy使用，请手工更改！
SQL替换命令解析：
 UPDATE 表名 SET 字段 = REPLACE(字段,’替换内容’,'替换值’);
示例如下：
 UPDATE wp_options SET option_value = REPLACE(option_value,'blog.zhaoxiao.li','blog.zhaoxiao.li');
这条语句的意思是：将表名为wp_options的字符段option_value的值由blog.zhaoxiao.li替换为blog.zhaoxiao.li。
好了，开始操作:
修改option_value里的站点url和主页地址：
 UPDATE wp_options SET option_value = REPLACE(option_value,’替换内容’,'替换值’);
更改文章中内部链接及附件的地址：
 UPDATE wp_posts SET post_content = REPLACE(post_content,’替换内容’,'替换值’);
更改wordpress文章默认的永久链接:
 UPDATE wp_posts SET guid = REPLACE(guid,’替换内容’,'替换值’);
更改博客用户里你的网站链接：（如果你的个人资料里没有填你的博客地址，可忽略）
 UPDATE wp_users SET user_url = REPLACE(user_url,’替换内容’,'替换值’);
更改评论者资料里你的博客链接：
 UPDATE wp_users SET user_url = REPLACE(user_url,’替换内容’,'替换值’);
更改评论内容你的博客链接：（如果评论里没有你博客链接，可忽略）
 UPDATE wp_users SET comment_content = REPLACE(comment_content,’替换内容’,'替换值’);
如果你没有安装No Self Pings插件，需要再执行以下操作：
 UPDATE wp_posts SET pinged = REPLACE(pinged,’替换内容’,'替换值’);
 UPDATE wp_posts SET to_ping = REPLACE(to_ping,’替换内容’,'替换值’);
到这里，全部完成了。

---


