---
title: ImmortalWrt的基本设置
date: '2026-06-06 00:00:00'
slug: ImmortalWrt-de-ji-ge-ji-ben-she-zhi
categories:
- 折腾
tags:
- 旁路由
- opwenclash
- openWRT
- 上网
---
最近折腾ImmortalWrt，遇到个坑，稍微折腾了下，这里用于记录！  

1)这里要设置网关，指向主路由。  

![](/assets/images/2026/06/06-1.png)
2)DNS服务器同样指向主路由. 
![](/assets/images/2026/06/06-2.png)
3）DHCP 这里忽略此接口. 
![](/assets/images/2026/06/06-3.png)
4）安全这里，如下勾选，并删除原本的WAN口转发. 
![](/assets/images/2026/06/06-4.png)

---


