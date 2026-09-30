# 个人博客

这是一个基于 GitHub Pages + Jekyll 的个人博客模板，适合写技术文章、生活记录、学习笔记和项目分享。

## 功能

- Markdown 文章发布
- 分类与标签页
- 图片展示与文章封面
- Utterances 评论系统
- 响应式博客主页
- GitHub Pages 一键部署

## 本地预览

```bash
bundle install
bundle exec jekyll serve --livereload
```

访问：http://localhost:4000

## 发布

直接推送到 GitHub 的 `main` 分支，GitHub Pages 会自动部署。

```bash
git add .
git commit -m "feat: setup personal blog"
git push origin main
```

## 文章示例

新文章放在 `_posts/` 目录下，命名格式：

```text
_posts/YYYY-MM-DD-文章标题.md
```

示例 Front Matter：

```yaml
---
layout: post
title: "我的第一篇文章"
date: 2026-09-30 09:00:00 +0800
categories: [技术]
tags: [GitHub Pages, Jekyll]
image: /assets/images/posts/cover.jpg
comments: true
---
```

## 目录说明

- `_posts/`：博客文章
- `_layouts/`：页面模板
- `_includes/`：可复用组件
- `assets/`：CSS、JS、图片
- `categories/`、`tags/`：分类与标签页面

## 备注

这个仓库已经配置为 GitHub Pages 站点，适合用来写博客，不依赖数据库，也便于长期维护。
