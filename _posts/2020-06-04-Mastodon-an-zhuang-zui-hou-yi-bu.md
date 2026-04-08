---
title: Mastodon 安装最后一步
date: '2020-06-04 00:00:00'
slug: Mastodon-an-zhuang-zui-hou-yi-bu
categories:
- 网络
tags:
- 网站
- gotosocial
---
在Mastodon安装最后一步，会遇到：
failed to enable unit: unit file mastodon-\x2a.service does not exist.
解决方法贴在这里，备用：
systemctl enable mastodon-web mastodon-sidekiq mastodon-streaming
(just replace the start with enable) or if you want to write it out:
systemctl enable mastodon-web
systemctl enable mastodon-sidekiq
systemctl enable mastodon-streaming

Notes (also for the docs):
Not all shells accept auto-completion for systemctl and are just trying to start a service named mastodon- (where the \x2a is the escaped ascii code from )

---


