---
title: Mastodon搭建-避坑指南
date: '2021-04-26 00:00:00'
slug: Mastodon-da-jian---bi-keng-zhi-nan
categories:
- 网络
tags:
- gotosocial
---
此指南基于官方安装教程：最后更新于 May 21, 2020。Mastodon为v3.3.0。

1. RUBY_CONFIGURE_OPTS=--with-jemalloc rbenv install 2.7.2
rbenv global 2.7.2
说明： 从3.3.0版开始， rbenv要用2.7.2版

2. bundle config deployment 'true'
bundle config without 'development test'
bundle install -j$(getconf _NPROCESSORS_ONLN)
yarn install --pure-lockfile
说明： 上文中加粗部分更换为：
bundle config deployment false
bundle update mimemagic --minor
bundle config deployment true
yarn install
否则会出现如下error：
mastodon@ION-Play:~/live$ bundle install -j$(getconf _NPROCESSORS_ONLN)
Fetching gem metadata from https://rubygems.org/............
Your bundle is locked to mimemagic (0.3.5) from rubygems repository
https://rubygems.org/ or installed locally, but that version can no
longer be found in that source. That means the author of mimemagic
(0.3.5) has removed it. You'll need to update your bundle to a version
other than mimemagic (0.3.5) that hasn't been removed in order to
install.

---


