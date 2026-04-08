---
title: Gotosocial 增加管理员账户&后期维护
date: '2022-12-24 00:00:00'
slug: Gotosocial-zeng-jia-guan-li-yuan-zhang-hu--hou-qi-wei-hu
categories:
- 转载
tags:
- docker
- 数据库
- 软件
- gotosocial
- Apple
---
在gotosocial目录下执行
1. 创建第一个用户的账号（替换some__username为你想要的用户名，someone@example.com为你的邮箱（用于登录，不一定要真实的）， 'some_very_good_password'为'你的密码'（具体原理参考go-password-validator）
docker exec -it gotosocial /gotosocial/gotosocial admin account create --username some_username --email someone@example.org --password 'some_very_good_password'
2. 然后确认这个账号（替换some__username为你的用户名）
docker exec -it gotosocial /gotosocial/gotosocial admin account confirm --username some_username
3. 提升这个账号为管理员（替换some__username为你的用户名）
docker exec -it gotosocial /gotosocial/gotosocial admin account promote --username some_username

系统更新：

可以用Watchtower自动更新（设置凌晨4点自动检测更新）
docker run -d \
--name watchtower \
--restart unless-stopped \
-v /var/run/docker.sock:/var/run/docker.sock \
containrrr/watchtower -c \
--schedule "0 0 4   "

数据库的备份
直接备份~/gotosocial/data下的文件即可。可以用rclone之类的工具，用crontab定时备份。以后补。

内容来源：
[https://zhuanlan.zhihu.com/p/531358936?utm_id=0](https://zhuanlan.zhihu.com/p/531358936?utm_id=0)
[https://docs.gotosocial.org/en/latest/installation_guide/docker/](https://docs.gotosocial.org/en/latest/installation_guide/docker/)

---


