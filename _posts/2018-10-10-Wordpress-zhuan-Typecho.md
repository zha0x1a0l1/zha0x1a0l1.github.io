---
title: Wordpress转Typecho
date: '2018-10-10 00:00:00'
slug: Wordpress-zhuan-Typecho
categories:
- 网络
tags:
- jekyll
- 数据库
---
转换堪称完美，具体步骤如下。
1. 当然是先安装好typecho， 记录好数据库名，用户名，密码。因为一会还要用。
2.进入typecho后台，安装 wordpresstotypecho_v1.0.3插件，并启用。
3. 插件设置处填好刚刚记录的wordpress数据库名，用户名，密码，其他保持默认。（如果你wordpress前缀有修改，记得这里也修改下）
4. 下载wordpress数据库， 并直接导入到typecho的数据库里。
4. 后台-控制台-从wordpress导入数据。放心点吧，保证成功。
5. 打包下载wordpress里的upload文件夹， 并上传到typecho的/usr目录下面。
6. SQL 执行 UPDATE typecho_contents SET text = REPLACE(text,'/uploads/','https://yantou.site/usr/uploads/');。 返回首页看看吧！

DEMO如本站： [https://yantou.site/](https://yantou.site/)

Notice: 其实本人并不推荐做这种转换。wordpress虽然臃肿，但这么多年来的持续更新，丰富的模板和插件， 是typecho所不能及的。typecho 3年未更新，去年突然诈尸了。还不知道能活多久。

---


