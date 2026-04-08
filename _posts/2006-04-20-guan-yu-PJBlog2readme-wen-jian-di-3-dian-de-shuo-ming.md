---
title: 关于PJBlog2 readme 文件第3点的说明
date: '2006-04-20 00:00:00'
slug: guan-yu-PJBlog2readme-wen-jian-di-3-dian-de-shuo-ming
categories:
- 网络
tags:
- jekyll
- 网站
- 数据库
- Linux
- 软件
---
在 PJBlog2 的readme文件里有这样的说明：

安装（Install）

-------------------------------------------------------------------------------

1. 到PJBlog2官方网站下载 "PJBlog2 2.5.0125"

2. 解压缩文件,然后把上传到服务器

3. 修改const.asp里面的数据库路径和Cookie名称,以确保你的站点安全

4. 用管理员用户登录

用户名:admin 密码:admin888

5. Enjoy!!!

其中的第三点好多朋友不知道怎么改，论坛上也没有详细的说明，我就以我的方法来说明一下．

打开const.asp有下面的文字：

'定义 Cookie,Application 域，必须修改，否则可能运行不正常

Const CookieName="PJBlog2"

Const CookieNameSetting="PJBlog2Setting"

分别把PJBlog2，PJBlog2Setting改名，至于什么名字吗？就随便你了．

'定义数据库链接文件，根据自己的情况修改

Const AccessFile="blogDB/PBLog2.asp"

把数据库路径blogDB/PBLog2.asp改掉，比如改成zxcf/PBLog2.asp ．改好后把你根目录下面的数据库文件夹改成相应的名字．

就OK了．
[Hhdcr]

---


