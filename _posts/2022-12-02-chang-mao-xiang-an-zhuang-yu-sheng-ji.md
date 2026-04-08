---
title: 长毛象安装与升级
date: '2022-12-02 00:00:00'
slug: chang-mao-xiang-an-zhuang-yu-sheng-ji
categories:
- 网络
tags:
- gotosocial
- JavaScript
---
遇到了几个小错误，记录一下。
1. Ruby version has been bumped to 3.0.4
2. 如下兼容性问题可跳过
yarn install --ignore-engines
RAILS_ENV=production bundle exec rails assets:precompile --ignore-engines
[1/6] Validating package.json...
error @mastodon/mastodon@: The engine "node" is incompatible with this module. Expected version ">=14". Got "12.22.12"
error Found incompatible module.
info Visit https://yarnpkg.com/en/docs/cli/install for documentation about this command.
Compiling...
3. 禁用未登录用户浏览
环境变量中设置 DISALLOW_UNAUTHENTICATED_API_ACCESS=true

---


