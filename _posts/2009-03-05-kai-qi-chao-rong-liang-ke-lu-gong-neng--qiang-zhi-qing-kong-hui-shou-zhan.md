---
title: 开启超容量刻录功能&强制清空回收站
date: '2009-03-05 00:00:00'
slug: kai-qi-chao-rong-liang-ke-lu-gong-neng--qiang-zhi-qing-kong-hui-shou-zhan
categories:
- 杂项
tags:
- 软件
---
27、Get more data onto CD-R discs（在光盘上刻录更多文件）
To enable overburn for Nautilus’ CD/DVD Creator (Places ! CD/DVD Creator), entirely at your own risk, open gconf-editor and head over to /apps/nautilus-cd-burner. Then put a check alongside overburn on the right.
(打开 Nautilus的CD/DVD 创建者超内容刻录功能，按Alt+F2，输入gconf-editor ,依次找到/apps/nautilus-cd-burner ,将右边的overburn钩选。)
39、Empty the trash even if told you can’t（强制清空回收站）
open a terminal window and type the following command,
（在终端输入：）
sudo rm -rf ~/.local/share/Trash/{files,info}/

---


