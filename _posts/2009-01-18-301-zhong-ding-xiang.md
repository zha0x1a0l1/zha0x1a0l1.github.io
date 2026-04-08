---
title: 301重定向
date: '2009-01-18 00:00:00'
slug: 301-zhong-ding-xiang
categories:
- 科技
tags:
- jekyll
- 工作
- 网站
- Linux
- 域名
---
更换域名，等于全新建立了一个博客，对于搜诉引擎，会有很大的影响。对旧域名进行重定向操作，就能避免了404页面。这样对博客的影响最小。
操作方法：（只适合linux的主机空间）
修改旧空间跟目录的.htaccess文件。如果是Windows系统系统下操作，可以新建立文本文档，修改好后上传到空间上再将文件名修改为.htaccess。
将.htaccess中的内容修改为：

# BEGIN WordPress

Options +FollowSymLinks
RewriteEngine on
rewritecond %{http_host} ^www.your-old-domain.com [nc]
rewriterule ^(.)$ http://www.your-new-domain.com/$1 [L,R=301]

# END WordPress
注意：进行重定向工作后，新域名博客内容的永久链接要与旧域名的永久链接格式保持一致。

---


