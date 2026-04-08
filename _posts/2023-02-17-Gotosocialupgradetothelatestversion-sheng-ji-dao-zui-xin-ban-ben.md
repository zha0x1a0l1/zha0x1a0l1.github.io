---
title: 2023 02 17 Gotosocialupgradetothelatestversion sheng ji dao zui xin ban ben
date: '2023-02-17 00:00:00'
slug: 2023-02-17-Gotosocialupgradetothelatestversion-sheng-ji-dao-zui-xin-ban-ben
categories:
- 网络
tags:
- gotosocial
- docker
---
---
title: Gotosocial: upgrade to the latest version/升级到最新版本
date: 2023-02-17 00:00:00
slug: Gotosocialupgradetothelatestversion-sheng-ji-dao-zui-xin-ban-ben
categories:
tags:
---

1. 进入搭建文件夹
cd gotosocial
2. 停止服务
docker-compose down
3.修改要升级的版本
nano docker-compose.yaml
4.拉取对应版本（0.7.0为例）
docker pull superseriousbusiness/gotosocial:0.7.0
5.启动服务
docker-compose up -d
6.确认没问题后，删掉旧的docker
docker system prune -a

---


