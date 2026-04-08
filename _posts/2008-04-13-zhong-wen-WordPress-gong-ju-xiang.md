---
title: 中文 WordPress 工具箱
date: '2008-04-13 00:00:00'
slug: zhong-wen-WordPress-gong-ju-xiang
categories:
- 网络
tags:
- jekyll
- Google
- Python
- 软件
---
老帖了，新转下！
用来解决官方 WordPress 没有照顾到的中文相关问题。使用这个插件，你可以显示随机文章，最新留言，留言最多文章，发表评论最多的网友，以及真正的文章摘要（如果你的模板里使用的是the_excerpt()来调用内容的话）等等，真正截断，没有乱码。

这个插件由 [WordPress 随机文章](http://yanfeng.org/blog/373/)和 [WordPress 评论插件](http://yanfeng.org/blog/479/)合并增强而来。在激活这个插件之前，请务必先停用这两个插件，不然的话会有冲突。

下载：mulberrykit.zip

安装：

解压缩，把 mulberrykit.php 上传至 /wp-content/plugins/
在管理界面里激活 中文 WordPress 工具箱插件（如果你在使用 [WordPress 随机文章](http://yanfeng.org/blog/373/)和 [WordPress 评论插件](http://yanfeng.org/blog/479/)，务必先停用这两个插件。）
使用说明：
1、最新回响

调用方式：get_recent_comments($no_comments = 5, $before = ‘-  ‘, $after = ‘
’, $show_pass_post = false)

$no_comments：显示回响数，缺省为5条；
$before：每条记录前显示的文字，缺省-
$after：每条记录后显示的文字，缺省

$show_pass_post：是(true)/否(false)显示保护了的文章，缺省否(false)

补充：
kdolphin 在回应里提出，希望在最新回响里不显示自己的回应。这很容易做到。在get_recentcomments() 这个函数里找到这一句

post_status = ‘publish’

在后面 加上

AND comment_author != ‘桑葚’

就可以了。（把上面的桑葚改成你自己的昵称；引号是半角的）

注意：最好在wp的插件编辑窗口下改，以免乱码的问题。

根据网友的建议加上了两个相关的函数：
仅显示留言，不包括引用
仅显示引用（包括trackback和pingback）

调用方式与相同。

2、最新文章

根据网友们的反馈，我把这个最新文章的函数又放回来了。

调用方式：get_recent_posts($no_posts = 5, $before = ‘- + ‘, $after = ‘
’, $show_pass_post = false, $skip_posts = 0)

$no_posts：显示文章数，缺省为5条；
$before：每条记录前显示的文字，缺省-
$after：每条记录后显示的文字，缺省

$show_pass_post：是(true)/否(false)显示保护了的文章，缺省否(false)
$skip_posts：跳过多少篇文章，缺省为0；

3、评论最多的帖子

调用方式：get_mostcommented($limit = 5)

4、发表评论最多的网友

把代码里面的blogmaster改成你自己的名字，可以滤掉你自己的名字。

调用方式：get_commentmembersstats($threshhold = 5)

5、随机文章

由[这个插件](http://www.w-a-s-a-b-i.com/archives/2004/05/27/wordpress-random-posts-plugin/)修改而来：
> a、改了提取excerpt摘要的方式，可适用于中文；
b、摘要可显示于文章链接的title里，或者直接在页面上，可选；
c、在文章链接的title里显示日期。

在模板里调用

调用方式: random_posts ($limit = 5, $length = 400, $before = ‘- ’, $after = ‘
’, $show_pass_post = false, $show_excerpt_in_title = true)

$limit：显示文章数，缺省5篇；
$length：摘要长度，缺省400；
$before：每条记录前显示的文字，缺省-
$after：每条记录后显示的文字，缺省

$show_pass_post：是(true)/否(false)显示保护了的文章，缺省否(false)
$show_excerpt_in_title：是(true)，摘要显示于文章链接的title；否(false)，直接显示于页面；缺省是(true)

6、显示摘要

某些情况下需要输出摘要，比如搜索结果、档案，还有 rss 输出，这样可以节省流量资源。但是，如果你的文章是中文的话，官方 WordPress 输出的其实并不是摘要，它只是把文章里的 html 代码过滤掉了，但所有文字都还是原样输出了。

激活这个插件后，输出的就是真正截断的摘要了。

原帖为：[http://yanfeng.org/blog/wordpress/kit/](http://yanfeng.org/blog/wordpress/kit/)

---


