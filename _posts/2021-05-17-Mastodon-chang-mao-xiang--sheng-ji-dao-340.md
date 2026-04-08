---
title: Mastodon(长毛象）升级到3.4.0
date: '2021-05-17 00:00:00'
slug: Mastodon-chang-mao-xiang--sheng-ji-dao-340
categories:
- 生活
tags:
- gotosocial
---
记录下升级过程，中间踩了几个小坑，折腾了一个多小时。
su - mastodon
bundle config deployment false
cd /home/mastodon/live
rm Gemfile.lock

---


