---
title: 使用Hexo+Anzhiyu搭建个人博客
date: 2026-06-15 13:00:00
categories:
  - 技术
tags:
  - Hexo
  - Anzhiyu
  - GitHub Pages
  - 教程
cover: /img/default_cover.jpg
---

## 前言

本文记录了使用 Hexo + Anzhiyu 主题搭建个人博客并部署到 GitHub Pages 的全过程。

<!-- more -->

## 环境准备

### 安装 Node.js

Hexo 需要 Node.js 环境，推荐使用 v20 或更高版本。

### 安装 Hexo CLI

```bash
npm install -g hexo-cli
```

## 初始化项目

```bash
hexo init my-blog
cd my-blog
npm install
```

## 安装 Anzhiyu 主题

```bash
cd themes
git clone https://github.com/anzhiyu-c/hexo-theme-anzhiyu.git anzhiyu
```

在根目录 `_config.yml` 中修改主题配置：

```yaml
theme: anzhiyu
```

## 部署到 GitHub Pages

### 1. 创建 GitHub 仓库

仓库名格式：`username.github.io`

### 2. 安装部署插件

```bash
npm install hexo-deployer-git --save
```

### 3. 配置部署信息

在 `_config.yml` 中添加：

```yaml
deploy:
  type: git
  repo: https://github.com/username/username.github.io.git
  branch: gh-pages
```

### 4. 部署

```bash
hexo generate
hexo deploy
```

## 日常写作流程

```bash
hexo new "文章标题"
# 编辑 source/_posts/文章标题.md
hexo generate
hexo deploy
```

## 总结

Hexo + Anzhiyu 是一个非常优秀的博客组合，Anzhiyu 主题功能丰富且美观，非常适合个人博客使用。
