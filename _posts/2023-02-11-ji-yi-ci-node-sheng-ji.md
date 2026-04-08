---
title: 记一次node升级
date: '2023-02-11 00:00:00'
slug: ji-yi-ci-node-sheng-ji
categories:
- 网络
tags:
- gotosocial
- JavaScript
- 数据库
---
mastodon最新版node已经要求14+了，上次升级就直接忽略了，这次索性折腾下。
Ruby: 2.7 to 3.0
PostgreSQL: 9.5 or newer
Elasticsearch (optional, for full-text search): 7.x
Redis: 4 or newer
Node: 14 or higher
1. 查看下当前node版本
node -v
2.清除npm缓存
npm cache clean -f
3. 安装n模块，用来管理node
npm install -g n
4. 更新升级node版本
 n stable // 把当前系统的 Node 更新成最新的 “稳定版本”
 n lts // 长期支持版
 n latest // 最新版
 n 10.14.2 // 指定安装版本
PS：因升级到最新版还要升级其他依赖，所以这次只升级到了14版。

---


