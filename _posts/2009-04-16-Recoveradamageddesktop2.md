---
title: Recover a damaged desktop
date: '2009-04-16 00:00:00'
slug: Recoveradamageddesktop2
categories:
- 杂项
tags:
- 软件
---
110、Recover a damaged desktop #2
If you’ve having trouble logging into your GNOME desktop, first see Tip 109. If that doesn’t work, you can try deleting your GNOME desktop configuration files and starting again. This is possible because, if GNOME doesn’t find configuration files where they should be, it will automatically create some afresh. Deleting these files is very radical because it will delete all your desktop settings, plus those for GNOME applications (although your Evolution mail and account settings will remain because they’re stored in the .evolution folder). However, if you have no other choice... Log out of the desktop and then switch to a new virtual console ( Ctrl + Alt + F2 ). Then login and type the following:
rm -rf .gnome-2
Then switch back to GUI mode ( Ctrl + Alt + F7 ) and login as usual.

---


