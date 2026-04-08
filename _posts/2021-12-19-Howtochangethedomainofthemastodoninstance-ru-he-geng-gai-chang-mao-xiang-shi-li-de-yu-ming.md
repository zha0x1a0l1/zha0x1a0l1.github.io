---
title: How to change the domain of the mastodon instance/如何更改长毛象实例的域名
date: '2021-12-19 00:00:00'
slug: Howtochangethedomainofthemastodoninstance-ru-he-geng-gai-chang-mao-xiang-shi-li-de-yu-ming
categories:
- 网络
tags:
- gotosocial
- 域名
- Nginx
- 服务器
---
注意：更改域名，相当于在宇宙中新建一实例。好处是省去了重新搭建的过程，所有嘟文依旧还在。坏处是，所有follower都无法自动获得新的嘟文。
下面是操作步骤：
1. 解析好新的域名到VPS
2. 修改配置文件
cd /home/mastodon/live
nano .env.production
3. 重新从Mastodon目录复制配置文件模版到nginx
cp /home/mastodon/live/dist/nginx.conf /etc/nginx/sites-available/mastodon
4. 替换 example.com 为你自己的域名
nano /etc/nginx/sites-available/mastodon
5.删掉原有域名SSL证书
sudo certbot delete
6. 为新域名重新申请SSL证书
certbot --nginx -d example.com

---


