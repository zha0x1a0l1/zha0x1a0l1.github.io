---
title: Mastodon 维护与备份
date: '2020-06-10 00:00:00'
slug: Mastodon-wei-hu-yu-bei-fen
categories:
- 技术
tags:
- 工作
- gotosocial
- 数据库
- 软件
---
定期清理：

su - mastodon
cd /home/mastodon/live
#计算被mastodon占用的空间
RAILS_ENV=production bin/tootctl media usage
#移除本地缓存的其它实例媒体附件
RAILS_ENV=production bin/tootctl media remove  --days=7
#清除缓存存储
RAILS_ENV=production bin/tootctl cache clear
#从数据库中删除未被引用的嘟文
RAILS_ENV=production bin/tootctl statuses remove
#移除本地预览卡片缩略图
RAILS_ENV=production bin/tootctl preview_cards remove
#扫描出不属于任何媒体附件的文件并移除他们
RAILS_ENV=production bin/tootctl media remove-orphans

定期备份：
准备工作： apt install lrzsz

1. PostgreSQL 数据库
su - mastodon
pg_dump mastodon_production > dump.sql
sz dump.sql
rm dump.sql
2. .env.production 文件或等效文件中的应用密钥
cd /home/mastodon/live
ls -a
sz .env.production
(应用密钥是最容易备份的，因为它们是不变的。你只需要将 .env.production 存储在安全的地方就可以了。)
3. 用户上传的文件
su - mastodon
cd live/public
tar -zcvf system.tar.gz system
sz system.tar.gz
rm system.tar.gz
如果你使用本地文件存储，复制体积巨大的 public/system 目录（默认存储上传文件的地方）
4. Redis 数据库
root
cd /var/lib/redis
sz dump.rdb
备份Redis是很容易的。Redis会定期将数据写入/var/lib/redis/dump.rdb文件，你只需要复制这个文件就可以了。

PS: 发送文件rz

---


