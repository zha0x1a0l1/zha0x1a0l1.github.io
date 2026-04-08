---
title: 开启root账户
date: '2009-04-16 00:00:00'
slug: kai-qi-root-zhang-hu
categories:
- 杂项
tags: []
---
111、Enable the root user（开启root账户）
assign the root user a password and thereby activate it
(激活root账户并为其设置密码)

sudo passwd root
Then type a new password that you’ll use in future when logging in as root user.
(然后输入你要设置的密码。(输入你当前用户的密码，然后再输入两次新的UNIX口令)。)
switch to root user at the command prompt by typing su
(在终端里输入su并输入密码，就能切换到root用户（注意：$变成了#）。)
You won’t be able to login as root from the login window
(但是在登陆窗口是不能用root账户登陆系统的。)
Click System ! Administration ! Login Window, then click the Security tab, and put a check in Allow Local System Administrator Login. Then close the program and log out and back in again as root (provide root as your username). Note that running a GUI as root is about as dangerous as it gets but, then again,it’s your computer!
(点击“系统-系统管理-登陆窗口-安全”，勾选“允许本地系统管理员登陆”。关闭，登出，在登陆的时候就可以用root账户登陆系统了（登陆时会有警告提示，点Continue继续）。注意：用root登陆并操作系统是很危险的事情。)

---


