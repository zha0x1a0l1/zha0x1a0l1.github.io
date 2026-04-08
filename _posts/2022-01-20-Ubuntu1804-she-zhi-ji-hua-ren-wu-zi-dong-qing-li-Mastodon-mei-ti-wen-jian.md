---
title: Ubuntu 18.04设置计划任务自动清理Mastodon媒体文件
date: '2022-01-20 00:00:00'
slug: Ubuntu1804-she-zhi-ji-hua-ren-wu-zi-dong-qing-li-Mastodon-mei-ti-wen-jian
categories:
- 转载
tags:
- jekyll
- Python
- Linux
- 服务器
- gotosocial
---
原文链接在这里，怕找不到，抄过来备用。
https://blog.error.im/index.php/archives/3/
由于Mastodon外站缓存文件会非常占用硬盘，并且很多站点都是在便宜的小硬盘vps上搭建所以非常有必要经常清理站外媒体文件。
我们可以通过设置Ubuntu计划任务来实现自动清理站外缓存。
我在Ubuntu18.04系统下按Mastodon官方文档教程搭建的实例。所以如果是用别的方式搭建的请忽略此文章。

su - mastodon //切换到Mastodon用户。
crontab -e //打开编辑器
写入以下代码
SHELL=/bin/bash
PATH=/home/mastodon/.rbenv/shims:/home/mastodon/.rbenv/bin:/usr/local/bin:/usr/bin:/bin
0 2 3 cd /home/mastodon/live && RAILS_ENV=production ./bin/tootctl media remove --days=15

SHELL=/bin/bash
PATH=/home/mastodon/.rbenv/shims:/home/mastodon/.rbenv/bin:/usr/local/bin:/usr/bin:/bin
0 3 3 cd /home/mastodon/live && RAILS_ENV=production /home/mastodon/live/bin/tootctl statuses remove --days=90

SHELL=/bin/bash
PATH=/home/mastodon/.rbenv/shims:/home/mastodon/.rbenv/bin:/usr/local/bin:/usr/bin:/bin
0 4 3 cd /home/mastodon/live && RAILS_ENV=production /home/mastodon/live/bin/tootctl media remove-orphans

SHELL=/bin/bash
PATH=/home/mastodon/.rbenv/shims:/home/mastodon/.rbenv/bin:/usr/local/bin:/usr/bin:/bin
0 5 3 cd /home/mastodon/live && RAILS_ENV=production /home/mastodon/live/bin/tootctl preview_cards remove --days=60

然后保存即可，它会在每周三 2点 3点 4点 5点 运行一次。

---


