---
title: Mastodon取消登录验证
date: '2022-04-02 00:00:00'
slug: Mastodon-qu-xiao-deng-lu-yan-zheng
categories:
- 杂项
tags:
- gotosocial
---
长时间不登陆，系统会要求验证码登录，对于没有设置发件服务的站点很是麻烦。可用如下命令解除：

su - mastodon
cd /home/mastodon/live
RAILS_ENV=production bin/tootctl accounts modify X1a0l1 --skip-sign-in-token

---


