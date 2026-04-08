---
title: Wordpress 搬家 更改域名
date: '2018-02-05 00:00:00'
slug: Wordpress-ban-jia--geng-gai-yu-ming
categories:
- 网络
tags:
- jekyll
- 网站
- 域名
- 搬家
---
需更改下面四行。

UPDATE wp_posts SET post_content = replace( post_content, '旧域名','新域名') ;
UPDATE wp_comments SET comment_content = replace(comment_content, '旧域名', '新域名') ;
UPDATE wp_comments SET comment_author_url = replace(comment_author_url, '旧域名', '新域名') ;
UPDATE wp_options SET option_value = replace( option_value , '旧域名','新域名') ;

---


