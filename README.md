# GitHub Pages 个人博客

这是一个基于 GitHub Pages + Jekyll 的个人博客模板，适合写技术文章、学习笔记和生活记录。

## 运行方式

```bash
bundle install
bundle exec jekyll serve --livereload
```

本地访问：

```text
http://localhost:4000
```

## 部署方式

直接推送到 `main` 分支，GitHub Pages 会自动部署。

```bash
git add .
git commit -m "feat: publish blog"
git push origin main
```

## 结构说明

- `_posts/`：博客文章目录
- `_layouts/`：页面模板
- `_includes/`：可复用组件
- `assets/css/`：样式文件
- `categories/`：分类页面
- `tags/`：标签页面
- `archive/`：归档页面
- `search/`：搜索页面
- `about.md`：个人介绍

## 推荐写作方式

1. 使用 Markdown 编写文章
2. 在 Front Matter 中写标题、日期、分类和标签
3. 把图片放在 `assets/images` 或文章相关目录
4. 持续维护归档和分类

## 适用场景

- 个人博客
- 技术记录
- 学习笔记
- 工作总结
- 生活随笔
