---
title: 长毛象(Mastodon) 搬家教程
date: '2021-02-23 00:00:00'
slug: chang-mao-xiang-Mastodon-ban-jia-jiao-cheng
categories:
- 网络
tags:
- Nginx
- Linux
- 数据库
- 搬家
- 服务器
---
1.在新的服务器上重新安装mastodon， 到“生成配置文件”之前结束。（也就是在执行RAILS_ENV=production bundle exec rake mastodon:setup之前）
2.停止旧服务器上的Mastodon（systemctl stop 'mastodon-.service'）
3. 导出并导入Postgres数据库

su - mastodon
pg_dump -Fc mastodon_production -f backup.dump
sz backup.dump

apt install lrzsz
su - mastodon
rz
createdb -T template0 mastodon_production
pg_restore -U mastodon -n public --no-owner --role=mastodon \
-d mastodon_production backup.dump
4. 复制 system/ 目录下文件

使用 root 权限进入到 system 这个文件夹的上一个目录
cd /home/mastodon/live/public
然后，使用 tar 命令将 system 目录传输到新服务器上：
tar czf  - system | ssh root@IP -p 端口 tar xzf - -C /home/mastodon/live/public
上面的命令执行后，会提示你输入新服务器的 SSH 连接密码，输入完毕之后，整个 SSH 窗口可能不会返回有效信息，等待一段时间，让服务器之间传输完成，直至你再次看到 SSH 窗口可以输入新执行命令时，就可以去新服务器上看看是不是传输完成了。
5. 复制 .env.production 文件

cd /home/mastodon/live
sz .env.production

cd /home/mastodon/live
rz
6. 编译mastodon
su - mastodon
cd /home/mastodon/live
RAILS_ENV=production bundle exec rails assets:precompile
RAILS_ENV=production ./bin/tootctl feeds build
exit
7. 从官网“配置 nginx”处继续安装

---


