---
title: CentOS7一键安装桌面环境
date: '2018-11-05 00:00:00'
slug: CentOS7-yi-jian-an-zhuang-zhuo-mian-huan-jing
categories:
- 科技
tags:
- 网站
- Python
- Linux
- 软件
- 开源
---
切换到管理员后，只需执行：
yum install curl ca-certificates -y && curl -sSL https://raw.githubusercontent.com/MeowLove/CentOS-One-click-Installation-of-Desktop-Environment-and-Remote-Desktop-Connection-RDP/master/download/main/install.sh | sudo bash
安装完成后，你就可以连接IP:3389（通过远程桌面连接）。默认RDP登陆账号：root，密码：你的root密码
脚本功能
1. 为您的Linux系统运行Windows应用程序。脚本自动帮你安装Wine X64和X86，现在可以在Linux上运行Windows应用程序。
2. 默认创建3GB交换内存。 避免内存不足导致的错误。（交换位置：/var/swapd）
3. 自动安装中文输入环境，中文支持。
4. 安装人们推荐的软件，例如浏览器和输入法。（包含Chrome，Firefox）
5. 安装远程桌面客户端。（支持RDP/SSH/NX/SFTP/VNC/XDMCP协议）
[![](/assets/images/2018/11/95420C56-C9AF-4513-B950-8687C9716386-450x338.jpeg)](/uploads/2018/11/95420C56-C9AF-4513-B950-8687C9716386.jpeg)

---


