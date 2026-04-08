---
title: Mastodon upgrade to 3.4.4
date: '2021-12-01 00:00:00'
slug: Mastodonupgradeto344
categories:
- 技术
tags:
- Git
- gotosocial
---
记录下升级方式：
su - mastodon
cd /home/mastodon/live

git config --global user.name "X1a0l1"
git config --global user.email "zhaoxiaoli@foxmail.com"

git stash
git fetch --tags
git checkout v3.4.4

---


