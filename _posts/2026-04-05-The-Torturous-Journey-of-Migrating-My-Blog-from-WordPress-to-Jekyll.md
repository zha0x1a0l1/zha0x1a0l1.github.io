---
title: 博客从 WordPress 到 jekyll 的折腾之路
date: '2026-04-05 00:00:00'
slug: The-Torturous-Journey-of-Migrating-My-Blog-from-WordPress-to-jekyll
categories:
- 杂项
tags:
- jekyll
- wordpress
- 博客
- 折腾
- GitHub
---
# 博客从 WordPress 到 jekyll 的折腾之路

最近花了两天时间把博客从 WordPress 迁移到了 jekyll，记录一下遇到的各种坑和解决方案。

## 背景

博客从 2006 年就开始写了，最早用 PJBlog，后来迁移到 WordPress，一晃快 20 年了。最近觉得 WordPress 太重了，决定迁移到静态博客。选择 jekyll + Chirpy 主题，部署到 GitHub Pages。

## 迁移过程

### 1. Hexo 源码转换

一开始有完整的 Hexo 博客源码，包含 959 篇文章。首先需要把 Hexo 的 Markdown 格式转换成 Jekyll 格式。

### 2. HTML 标签清理

从 WordPress 导出的文章残留大量 HTML 标签，需要批量清理：
- img 标签转换成 Markdown 图片语法
- a 链接转换
- HTML 实体转换（&nbsp; → 空格等）
- 移除 more 注释

### 3. 分类和标签重构

根据文章内容重新分类：生活、工作、爱情、网络、杂记、宝贝、科技、资讯、转载

## 遇到的问题及解决方案

### 问题一：jekyll 构建失败

**问题描述：** 本地构建时报错 invalid date 或 front matter 格式错误。

**解决方案：** 检查每篇文章的 front matter，确保 date 格式为 YYYY-MM-DD HH:MM:SS。

### 问题二：Slug 冲突

**问题描述：** 多篇文章生成相同的 URL，导致文件被覆盖。

**涉及的文章：** yan-lun 相关 5 篇文章，ai、yuan-dan-kuai-le、qi-qi-ba-ba-de-shi 等。

**解决方案：** 在文章 front matter 里手动修改 slug，给冲突的文章添加序号：slug: yan-lun-1、yan-lun-2 等。

### 问题三：htmlproofer 检查失败

**问题描述：** GitHub Actions 构建时 htmlproofer 工具报错 Addressable::IDNA::PunycodeBigOutput。

**原因：** 某篇文章包含特殊字符或超长 URL。

**解决方案：** 删除 GitHub Actions workflow 中的 Test site 步骤。

### 问题四：Git 游离状态

**问题描述：** 在 detached HEAD 状态做了提交，切换分支后提交变成了孤儿。

**解决方案：** git cherry-pick commit-hash 或 reset 后重新修改。

### 问题五：GitHub 推送被拒绝

**问题描述：** 远程仓库有新提交，本地落后。

**解决方案：** git pull --rebase 后再 push。

## 最终结果

- ✅ 962 篇文章成功迁移
- ✅ 所有 slug 冲突解决
- ✅ GitHub Pages 自动部署正常
- ✅ 博客访问地址：https://zhaox1a0l1.github.io/

## 总结

这次迁移主要是和 jekyll 的 URL 生成规则打交道。jekyll 默认使用文章的 slug 或标题生成 URL，如果多篇文章标题相同就会冲突。提前检查并修改冲突的 slug 是关键。

GitHub Actions 的 htmlproofer 工具比较严格，遇到特殊字符会报错，如果不需要严格的链接检查，直接禁用是更省心的方案。

---
*Posted on 2026-04-05*
*Author: 赵晓利