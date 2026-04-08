---
title: Blog Migration from WordPress to Hexo - Problems and Solutions
date: '2026-03-29 22:00:00'
slug: blog-migration-wordpress-to-hexo-problems-solutions
categories:
- 科技
tags:
- jekyll
- 网站
- JavaScript
- 开源
- 域名
---
# Blog Migration: WordPress to Hexo - Problems and Solutions

## Background

On March 29, 2026, I successfully migrated my blog from WordPress to Hexo static site generator and deployed it to GitHub Pages. This article documents the problems I encountered and how I solved them.

## Problems Encountered

### Problem 1: GitHub Pages 404 Error

Issue: After deploying to GitHub Pages, the blog showed 404 error for all posts.

Root Cause:
1. The GitHub branch was set to `main` instead of `master`
2. The GitHub Pages source was not properly configured
3. No `.nojekyll` file was added

Solution:
1. Changed GitHub Pages branch from `main` to `master`
2. Selected `/ (root)` as the source folder
3. Added `.nojekyll` file to prevent jekyll processing

### Problem 2: Chinese Characters in URLs Causing 404

Issue: Posts with Chinese characters in URLs returned 404 errors.

Root Cause: GitHub Pages couldn't properly handle URL-encoded Chinese characters.

Solution:
1. Installed `hexo-abbrlink` plugin to generate numeric IDs
2. Changed permalink format from `:title` to `:abbrlink`
3. Later changed to pinyin format for better readability

### Problem 3: Images Not Loading

Issue: All images showed 404 errors after migration.

Root Cause: Image URLs still pointed to the old WordPress server (`blog.zhaoxiao.li`).

Solution:
1. Copied all uploads from WordPress to Hexo's `source/uploads/` folder
2. Changed all image URLs from `https://blog.zhaoxiao.li/wp-content/uploads/` to `/uploads/`
3. Pushed uploads folder to GitHub repository

### Problem 4: Theme Not Working (Hingle)

Issue: After installing Hingle theme, the blog showed a blank page.

Root Cause:
1. Theme files were in `node_modules` instead of `themes` directory
2. Hexo couldn't find the theme layout files

Solution:
1. Moved theme files from `node_modules/` to `themes/` directory
2. Updated `_config.yml` to point to the correct theme folder
3. Ran `hexo clean && hexo generate` to rebuild

### Problem 5: Custom Domain Unbinding After Each Deploy

Issue: Had to manually rebind custom domain `blog.zhaoxiao.li` after every deployment.

Root Cause: CNAME file was not being copied to the `public` folder during generation.

Solution:
1. Created CNAME file in `source/` directory
2. Added post-generation task to copy CNAME to public folder
3. Now CNAME is automatically included in every deployment

### Problem 6: Server to GitHub Push Timeout

Issue: Git push from server to GitHub constantly timed out.

Root Cause:
1. DNS was hijacked to wrong IP (198.18.x.x)
2. Network routing issues between China and GitHub

Solution:
1. Added static routes to `/etc/hosts`:
   ```
   140.82.121.4 github.com
   140.82.112.4 www.github.com
   ```
2. Used GitHub Token for authentication instead of SSH
3. Increased Git buffer size with `git config http.postBuffer`

## Final Configuration

### Hexo Configuration
```yaml
permalink: posts/:slug.html
url: https://blog.zhaoxiao.li
deploy:
  type: git
  repo: git@github.com:zha0x1a0l1/blog.git
  branch: master
```

### Theme
Used Cactus theme - clean and elegant design.

### Custom Domain
- Domain: `blog.zhaoxiao.li`
- DNS: CNAME record pointing to `zha0x1a0l1.github.io`

## Summary

The migration from WordPress to Hexo was successful! Key achievements:

- ✅ 959 blog posts migrated with English URLs
- ✅ All images transferred to GitHub
- ✅ Custom domain configured and working
- ✅ Hexo source files synchronized between server and Mac
- ✅ CI/CD pipeline working smoothly

## Lessons Learned

1. Always check GitHub Pages branch settings
2. Use English or pinyin for URLs to avoid encoding issues
3. Keep Hexo source files in version control
4. Add CNAME to source folder, not just public folder
5. Server-to-GitHub push may need hosts file fixes in China

---

