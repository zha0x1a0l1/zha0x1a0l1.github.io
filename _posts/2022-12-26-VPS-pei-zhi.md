---
title: VPS配置
date: '2022-12-26 00:00:00'
slug: VPS-pei-zhi
categories:
- 网络
tags:
- 网站
- Git
- Python
- 服务器
---
一般，系统装好后，会做如下简单安全设置：
安装常用命令
apt update && apt install wget rsync python git curl vim git ufw -y
配置防火墙
sudo ufw allow OpenSSH
sudo ufw enable
打开防火墙，随后打开80和443端口：
sudo ufw allow http

---


