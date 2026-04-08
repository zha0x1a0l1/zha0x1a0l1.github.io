---
title: 安装所有多媒体解码器
date: '2009-03-12 00:00:00'
slug: an-zhuang-suo-you-duo-mei-ti-jie-ma-qi
categories:
- 网络
tags:
- Linux
- 软件
---
65、Install all the multimedia playback codecs you’ll ever need（安装所有多媒体解码器）
click Applications ! Add/Remove and then, in the Show dropdown list, select All Available Applications. Ensure All is selected in the list on the left, and then use the Search box to search for gstreamer. In the list of results, put a check alongside the following—once done, click the Apply Changes button:
(在“添加/删除程序”里查找并安装：)

GStreamer extra plugins
GStreamer ffmpeg video plugin
Ubuntu restricted extras
GStreamer plugins for mms, wavpack, quicktime, musepack
GStreamer plugins for aac, xvid, mpeg2, faad
GStreamer fluendo MPEG2 demuxing plugin
enable DVD movie playback
(添加DVD播放支持：)

sudo /usr/share/doc/libdvdread3/install-css.sh
Note that you will need to install the Xine version of Totem Movie Player if you want fuss-free DVD movie playback.
(安装Xine和Totem播放器来播放DVD。)

---


