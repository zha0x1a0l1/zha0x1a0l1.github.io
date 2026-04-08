---
title: 简单5步，制作wordpress留言板
date: '2007-10-21 00:00:00'
slug: jian-dan-5-bu--zhi-zuo-wordpress-liu-yan-ban
categories:
- 转载
tags:
- jekyll
- 网站
- Python
- 服务器
---
做一个wordpress留言板很简单，我们知道一般可以用新建一个主题名字叫“留言板”的页面，让访客以评论留言的方式来实现。但是这种方式建立的留言板，其实是一个一般主题(post)或页面(page)，因此缺乏进一步定制的功能，而且提示文字也全部是“评论”
要做一个可定制的留言板其实很简单，只需要5步，那就让我们开始吧:)
如果你满足下列要求，请继续，
 你有主机文件存储权限(一般博客服务提供商可能没有提供此权限).
 你可以以admin权限登录后台(一般都有吧)
 你大概知道点HTML和PHP文本形式的差别(定制部分需要修修改改，当然不难，只要认得出什么是html文本，什么是php文本就及格).
一：制作留言板模板：
1）找到你博客模板目录中的single.php文件（一般你的模板目录是在/wp-content/themes/博客模板名称/）；复制 single.php并重命名为guestbook.php,这样做的目的是我们希望留言板能保持博客的基本布局如：页面头部，页脚和侧边栏。因此最好的方式就是复制用来显示单篇主题的页面模板文件single.php
2）用一款合适的文本编辑器（如：editplus，ultraedit，notepad2，之所以没说windows自带的notepad是因为它对UTF-8的编码方式支持不好）；打开guestbook.php 在文件头部找到如下php代码：

在此语句前加一段仅带注释语句的模板标识，这里我们将页面模板名字(Template Name)定义为Guestbook，这个名字在下面会有用到。

OK，简单吧，留言板的页面模板文件就做好了。
3）将修改后的guestbook.php上传到博客模板目录(/wp-content/themes/博客模板名称/)下
二：在后台创建留言板
4）以具有admin权限的帐号登录，新建一个页面，在主题名称处输入“留言板”，在内容处像往常写博客主题一样输入些内容，如：请留下宝贵意见和建议等等
5）很重要的一步：在右侧页面模板(page template)处(见图)，选择刚才创建的guestbook页面模板，发布(publish)，完成。
去自己的博客主页看看，根据博客模板的不同，留言板会以Tab方式或者侧栏链接的方式显示
三：把留言板做的更完美
通过上面的5步，你已经拥有一个留言板了，但是这和新建主题/页面生成的留言板没什么区别。别急，因为我们的留言板是根据自建的guestbook页面模板生成的，所以做适当的修修改改就可以了，而且这并不会影响到其他一般主题或页面的显示
1）去掉发布日期：
如果你不希望你的留言板主题显示如一般主题那样的发布日期，那么在guestbook.php中找到如下代码并删除。
 (根据不同模板不同可能有点不同，比如可能是)
2）自定义“留言”样式的提示文本
因为其他主题或页面的评论都是用到comments.php来显示和输入评论的，不能把那些地方的“评论”也改成“留言”了。
因此复制一份comments.php并命名为guestcomments.php，就在guestcomments.php上修修改改吧
把所有“X comments”(xxx条评论)改成“X guestbook entries”(xxx条留言)
把“Post Comment”(发布评论)按钮的提示改成“Sign Guestbook”(发布留言)
3）最新留言显示在顶部
按照评论方式的留言，总是最新的留言排在最下面，如果我们希望最新的留言显示在最上面，可以这么做
在guestcomments.php中找到如下代码：
foreach ($comments as $comment)
替换成
foreach (array_reverse($comments) as $comment)
好啦，自定义的留言文本和显示方式据改好了，最后别忘了把guestcomments.php上传到你的博客模板目(/wp-content/themes/博客模板名称/)下
4）仅仅修改上面的2),3)；原来的guestbook.php并不知道你想启用新的留言和显示方式，所以我们还是要回到guestbook.php(不会那么快忘记这个文件吧:) )
找到如下代码：

替换成

四：还有什么花样吗?
因为我们用的是guestbook.php作为留言板的页面模板，相比一般主题/页面生成的留言板, 通过修改guestbook.php, 我们能获得更多的功能和提示，因为我们能在此文件中加入php语句，可以是自编的，也可以是其他插件中引用过来的函数。
这也给了我们一个启示，就是通过自定义页面模板的方式，我们可以定义一个全新页面，可以保留侧栏(sidebar)，页脚(foot)，也可以不保留，然后在内容(content)部分加入自己的php代码。

原文转自：[http://blog.yepn.net/archives/167](http://blog.yepn.net/archives/167)

---


