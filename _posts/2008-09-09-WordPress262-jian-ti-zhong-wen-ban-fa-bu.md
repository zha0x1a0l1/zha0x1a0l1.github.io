---
title: WordPress 2.6.2 简体中文版发布
date: '2008-09-09 00:00:00'
slug: WordPress262-jian-ti-zhong-wen-ban-fa-bu
categories:
- 科技
tags:
- jekyll
- Google
- 网站
---
本次更新，主要是修正了一些 Bug，并且排除了多处安全隐患。所以，如果您使用的是 WordPress 2.6.1 或更老的版本，强烈建议您进行升级。
本次中文版本发布，共修改了两个核心文件：
wp-config-sample.php 文件：将其中的说明文字汉化为简体中文，并且修改默认语言为 zh_CN。
readme.html 文件：对该说明文档进行完全汉化。
下载地址：http://code.google.com/p/wpcn/downloads/list
本中文版由WordPress中文团队制作，做了以下修改（相对于英文原版）：
    加入wp-content/languages/zh_CN.mo中文包；
    加入了 zh_CN.po，方便大家对中文包自行修改；
    修改wp-config-sample.php中的“define (’WPLANG’, ”);”为“define (’WPLANG’, ‘zh_CN’);”；
    汉化readme.html文件；
    加入中文 Dashboard 插件，方便大家得到更多的中文信息（插件需用户自行启动）
请按以下步骤进行升级：
    备份你修改过的文件，并上传新版本文件直接覆盖掉旧版本文件；
    上传所有新文件；
    在浏览器中打开 http://您博客地址/wp-admin/upgrade.php；
    升级完成。

---


