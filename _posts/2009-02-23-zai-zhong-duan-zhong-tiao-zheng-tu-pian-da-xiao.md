---
title: 在终端中调整图片大小
date: '2009-02-23 00:00:00'
slug: zai-zhong-duan-zhong-tiao-zheng-tu-pian-da-xiao
categories:
- 转载
tags: []
---
11、Shrink or enlarge images at the command line（在终端中调整图片大小）
you’ll need to install it via Synaptic (search for and install imagemagick)
(通过新立得安装imagemagick)
For example, the following will shrink filename.bmp to half its original size:
(例如，通过下面的命令可以将filename.bmp的图片调成原来的一半大小（调整一半大小后的文件为filename_small.bmp）：)

convert -resize 50% filename.bmp filename_small.bmp
The following will enlarge filename.bmp to twice its original size (although there will be an obvious degradation in quality):
(通过下面的命令可以将图片放大两倍（图像可能会失真）)

convert -resize 200% filename.bmp filename_larger.bmp
PS:图像需事先放到home 文件夹下

---


