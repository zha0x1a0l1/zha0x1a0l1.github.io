---
title: Wordpress的相册插件
date: '2008-02-25 00:00:00'
slug: Wordpress-de-xiang-ce-cha-jian
categories:
- 网络
tags:
- jekyll
- Python
- JavaScript
---
推荐Wordpress相册插件，[NextGEN Gallery 0.83 ](http://alexrabe.boelinger.com/?page_id=80)，官方出了[中文语言包](http://alexrabe.boelinger.com/wp-content/download/lang/nggallery-zh_CN.zip)，这个插件具有如下功能：
1. 可以通过拖拉进行相册的排序，跟 widget 一樣样，你想要怎么排序用拉就可以，所见既所得 !
2. 浮水印功能，可在照片上加上文字或图片。
3. 可以上传图片的压缩文件 (zip)，或直接导入图片的文件夹，懒人的最爱，省去上传的时间。
4. 內建 JavaScript 效果 ，Thickbox，Greybox or Lightbox ，效果很炫。
5. 可自己编辑CSS文件，通过 css 你可以打造属于自己的相册风格 !
6. Slideshow - 自动播放图片，还有许多变化效果。
7. Sidebar Widget - 随机显示图片的 widget ，可以显示在 sidebar 內。
8.可以在文章内调用图片，与附件完美整合到编辑页面的选择栏内，太方便了。
更多功能还有N多。。。
插件安装：
1. 下载[NextGEN Gallery 0.83 ](http://alexrabe.boelinger.com/?page_id=80)和[中文语言包](http://alexrabe.boelinger.com/wp-content/download/lang/nggallery-zh_CN.zip)，将解压后的语言包文件放到nextgen-gallery文件夹下的lang文件夹下。
2. 下载[JW Image Rotator](http://www.jeroenwijering.com/upload/imagerotator-3-15.zip) ，将解压出来的imagerotator.swf放到nextgen-gallery文件夹下。（imagerotator.swf只是一个flash播放器，为了实现相册的幻灯片效果）
3. 将插件传到wp-content/plugins/目录下，后台激活就可以了。

4.在wp-content目录下新建gallery文件夹，并将文件夹属性设置为777.这里就是存放你的图片的地方。

登陆到后台就可以看到“影集”了，这就是你的相册，接下来要做的就是建立自己的相册了。

1.后台“影集”->“相册”，“添加新相册”，这里把你要添加的相册添好，点“更新”，相册就建立好了。

2.后台“影集”->“添加影集”，“新影集”，这里是建立相册下面的小的分类，输入影集名，点“添加影集”，新的影集就建立好哦了。系统会自动在wp-content/gallery/建立影集文件夹。

3.返回后台“影集”->“相册“处，是不是影集已经建立好了呢？

![24552863.jpg](/assets/images/2008/02/24552863.jpg)

4.新写一个页面，写入或(写的时候请将“”号换成“[]”，要不，我这里就直接显示我的相册了)。这个作用是相册的前台显示。

5.后台”影集“->“管理影集”->“编辑”，对相册进行设置

![ffdfdfd.jpg](/assets/images/2008/02/ffdfdfd.jpg)

“页面连接到”选择刚刚写的新页面，“预览图像”为设置相册的封皮。设置好后“保存更新”就好了。

说明一、右边的影集可以通过拖放的形式拉到不同的相册下，对影集的排序也可通过拖放形式来完成。是不是很酷的功能。拖放好后别忘记点”更新“哦。

说明二、图片的上传可以有上传一个ZIP文件，导入图片文件和上传图片三种形式。其中导入图片文件方式最为方便，直接在你的wp-content/gallery/目录下建立好文件夹，把图片上传到文件夹下，在后台的”影集“->“添加影集”->“导入图片文件”,在“导入图片文件夹”处添好你刚刚建立的文件夹名，点“导入文件夹”，这样你的图片就上传好了。

说明三、相册的前台显示，新写一个页面，用“源代码“方式写入或(写的时候请将“”号换成“[]”，要不，我这里就直接显示我的相册了)。后面的数字为你的相册或影集的ID号，在后台的”影集“->”相册“处就可以看的到相册或影集的ID号。其中[album=ID]的显示效果是显示一个相册，就像[我的相册](http://blog.zhaoxiao.li/gallery)上面的那个那样。[gallery=ID]的显示效果是一个影集，它会把相册文件夹里的图片都并排显示出来，就像[我的相册](http://blog.zhaoxiao.li/gallery)下面的那个那样。

当然，相册还有更多的功能及更多的显示方法，这个相册目录下的readme.txt文件有详细说明，就自己去发觉吧。That's all, Good luck!

---


