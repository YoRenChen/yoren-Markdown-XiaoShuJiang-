---
title: Hexo - GitHub 装饰个人博客
tags: hexo, GitHub, 个人博客建设
grammar_cjkRuby: true
---

## 简介
在我们初次搭建完博客的同时，自己的博客看起来就像毛坯房一样，那么我们接下来需要按照自己的设计图进行装修，本文会带来是：
1. 有哪些装饰手段
2. 怎么进行装饰

## 深入了解Hexo
引用NexT文章中对Hexo的配置文件的解释：
> 在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
为了描述方便，在以下说明中，将前者称为 **站点配置文件**， 后者称为 **主题配置文件**。

## 使用NexT装饰
[NexT官网][1]
使用NexT的原因是精简。
### 下载NexT
【克隆】在终端窗口下，定位到 Hexo 站点目录下。使用 Git checkout 代码：
``` stylus
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```
【下载】
前往 [发布页][2] 下载版本
解压所下载的压缩包至站点的 themes 目录下， 并将 解压后的文件夹名称（hexo-theme-next-0.4.0）更改为 next。

  [1]: https://theme-next.iissnan.com/getting-started.html
  [2]: https://github.com/iissnan/hexo-theme-next/releases