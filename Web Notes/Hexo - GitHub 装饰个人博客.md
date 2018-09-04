---
title: Hexo - GitHub 装饰个人博客
tags: hexo, GitHub, 个人博客建设
grammar_cjkRuby: true
---

[toc]

## 简介
在我们初次搭建完博客的同时，自己的博客看起来就像毛坯房一样，那么我们接下来需要按照自己的设计图进行装修，本文会带来是：
1. 哪些装饰手段
2. next安装
3. 如何用next进行装饰

## 了解Hexo
引用NexT文章中对Hexo的配置文件的解释：
> 在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml。 其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
为了描述方便，在以下说明中，将前者称为 **站点配置文件**， 后者称为 **主题配置文件**。

这里默认的主题为**landscape**，在`themes - landscape`里。
## 使用landscape

## 使用NexT装饰
[NexT官网][1]
使用NexT的原因是精简。
### 下载NexT
【克隆】
在终端窗口下，定位到 Hexo 站点目录下。使用 Git checkout 代码：
``` stylus
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```
【下载】
前往 [发布页][2] 下载版本；

### 使用
1. 解压所下载的压缩包至站点的 themes 目录下， 并将解压后的文件夹名称**hexo-theme-next-x.x.x更改为 next**，否则运行的时候会白屏，debug会提示`No layout: index.html`。
2. 与所有 Hexo 主题启用的模式一样。 当 克隆/下载 完成后，打开 **站点配置文件**， 找到 `theme` 字段，并将其值更改为 `next`。

### 调试
使用`hexo debug`进行本地调试
跟换的时候最好使用 hexo clean 来清除 Hexo 的缓存。

## NexT装饰风格
【计划】
1.首页为独立的首页，可以展示个人信息，内容简介等。
2.首页侧栏（标签分类，文章目录，站点概览）。
3.首页文章预览为概要浏览而非全文

### 首页文章不显示全文
- 项目的themes/next目录
- 打开 **config.yml**文件，修改**auto_excerpt**里的**enable**为true

### 修改首页摆放模式
![enter description here][3]

### 标签tags
在页面上生成tags需要两个步骤：
1.生成“标签”。
2.文章中添加标签。

【生成tags】
执行：`hexo new page tags`
![][4]
打开文件并添加`type: 'tags'`

``` stylus
---
title: tags
date: 2018-09-04 20:18:43
type: 'tags'
---
```
在**config.yml**中找到menu添加`  tags: /tags` 
![][5]
我们就创建了tags标签。

注意，如果只是在**config.yml**中添加虽然在导航栏出现，但访问会出现404。

----------
【文章添加标签】
创建文章：`hexo new [layout(post/page/draft)] <name>` 
添加标签：

``` stylus
---
layout: page
title: tessst
date: 2018-09-04 20:21:51
tags:
    - 123
---
```
效果：
![enter description here][6]
访问进去：
![enter description here][7]

---------

### 分类Categories
1.生成categories并添加tpye属性
2.文章添加“Categories”属性

【生成categories并添加tpye属性】
执行：`hexo new page categories`
![][8]

找到文件并添加：
``` stylus
---
title: categories
date: 2018-09-04 22:36:40
type: "categories"
---
```
【文章添加分类】

``` stylus
---
layout: pages
title: tessst
date: 2018-09-04 20:21:51
tags:
    - 123
categories:
    - hexo创建标签
---
```
![enter description here][9]

![enter description here][10]

-------


  [1]: https://theme-next.iissnan.com/getting-started.html
  [2]: https://github.com/iissnan/hexo-theme-next/releases
  [3]: ./images/1535389772099.jpg
  [4]: ./images/1536068847445.jpg
  [5]: ./images/1536069060347.jpg
  [6]: ./images/1536070688519.jpg
  [7]: ./images/1536070719368.jpg
  [8]: ./images/1536071818930.jpg
  [9]: ./images/1536072297386.jpg
  [10]: ./images/1536072309496.jpg