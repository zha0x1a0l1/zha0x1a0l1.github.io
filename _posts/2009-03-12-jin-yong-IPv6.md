---
title: 禁用IPv6
date: '2009-03-12 00:00:00'
slug: jin-yong-IPv6
categories:
- 网络
tags:
- 域名
- 软件
---
60、Avoid network slowdowns and incompatibilities（禁用IPv6）
1. Open a terminal window and type gksu gedit /etc/modprobe.d/aliases. In the Gedit window, look for the line that reads alias net-pf-10 ipv6 and change ipv6 to off, so it reads alias net-pf-10 off. Then save the file.
(在终端里输入)
gksu gedit /etc/modprobe.d/aliases
(找到alias net-pf-10 ipv6 这行，修改为alias net-pf-10 off ，保存后退出。)
2. Open the /etc/hosts file in Gedit (gksu gedit /etc/hosts) and, after the line that reads # The following lines are desirable for IPv6 capable hosts, put a hash at the beginning of each line following that contains ip6 within it (so the first line will read #::1 ip6-localhost ip6-loopback; the second #fe00::0 ip6-localnet, and so on).
(在终端输入)
gksu gedit /etc/hosts
(将# The following lines are desirable for IPv6 capable hosts 这行下面的每一行前都加上#号。保存后退出。)
3. Start Firefox and, in the address bar, type about:config. You can ignore the warning that appears about changing settings. In the Filter text field, type ipv6. Then double-click network.dns.disableIPv6 so that it now appears in bold (and you might notice that, at the end of the line, false changes to true). Then close Firefox and reboot
your computer.
(打开 firefox, 在地址栏输入 about:config ,在“过滤器”框输入 ipv6。双击“network.dns.disableIPv6“。（双击后，值由false变为ture）关闭firefox 重起系统。)

---


