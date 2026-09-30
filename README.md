# 此间文字 — 个人文学博客

私人归档，自我梳理。记录所见、所思、所读。

## 本地启动

### 方式一：新终端（推荐）

打开 PowerShell，依次执行：

```powershell
# 1. 把 Ruby 加入 PATH（每次新终端都要执行）
$env:Path = "C:\Ruby32-x64\bin;$env:Path"

# 2. 进入项目目录
cd C:\Users\lenovo\Desktop\BosBoss

# 3. 启动本地服务器
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

看到 `Server running...` 后，浏览器打开：

```
http://127.0.0.1:4000/
```

### 方式二：一键脚本

直接在项目根目录运行：

```powershell
& "C:\Users\lenovo\Desktop\BosBoss\start.ps1"
```

（见下方说明）

### 停止服务器

在运行 Jekyll 的终端窗口按 `Ctrl + C` 即可。

## 常用页面地址

| 页面     | 地址                        |
| -------- | --------------------------- |
| 首页     | http://127.0.0.1:4000/      |
| 分类     | http://127.0.0.1:4000/categories/ |
| 标签     | http://127.0.0.1:4000/tags/       |
| 时间长河 | http://127.0.0.1:4000/archive/    |
| 关于     | http://127.0.0.1:4000/about/     |
| RSS      | http://127.0.0.1:4000/feed.xml   |

## 写新文章

在 `_posts/` 目录下新建文件，命名格式 `YYYY-MM-DD-标题.md`，头部：

```yaml
---
layout: post
title: "文章标题"
date: 2026-09-30 10:00:00 +0800
categories: [职场札记]        # 五选一：职场札记/读书漫笔/文存摘录/自撰集/碎语集
tags: [职场人际, 内耗, "2026"]  # 注意：年份数字要加引号
image: /assets/images/posts/xxx.jpg  # 可选，封面图
featured: true                       # 可选，设为精选文章
source: 原文出处                     # 摘录类文章必填
---
```

保存后本地服务器会自动刷新，浏览器刷新即可看到新文章。

## 安装依赖（仅首次需要）

```powershell
$env:Path = "C:\Ruby32-x64\bin;$env:Path"
cd C:\Users\lenovo\Desktop\BosBoss
bundle install
```

## 部署到 GitHub Pages

```powershell
& "C:\Program Files\Git\cmd\git.exe" add .
& "C:\Program Files\Git\cmd\git.exe" commit -m "发布博客"
& "C:\Program Files\Git\cmd\git.exe" push origin main
```

推送后 GitHub Actions 会自动构建部署。

## 项目结构

```
BosBoss/
├── _posts/          文章目录
├── _layouts/        页面模板（default/post/page）
├── _includes/       可复用组件（header/footer/comments）
├── _sass/           样式源文件
├── assets/images/   图片资源
├── categories/      分类页
├── tags/            标签页
├── archive.md       时间长河（归档页）
├── about.md         关于页
├── index.html       首页
├── _config.yml      Jekyll 配置
└── Gemfile          Ruby 依赖
```

## 五大分类

| 分类     | 用途                           |
| -------- | ------------------------------ |
| 职场札记 | 职场观察、人际感悟、工作思考   |
| 读书漫笔 | 完整读书笔记、读后感、书籍拆解 |
| 文存摘录 | 网文精品片段、经典段落摘抄     |
| 自撰集   | 原创随笔、短文、故事、文案     |
| 碎语集   | 经典语录、短句、碎片感悟       |
