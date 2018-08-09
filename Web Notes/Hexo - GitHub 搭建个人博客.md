---
title: Hexo - GitHub 搭建个人博客
---


## 简介
利用GitHub上的空间和功能可以快速搭建起个人的博客，其次Hexo更加简便地控制样式。
在Hexo - GitHub 搭建个人博客分为两步：
- GitHub创建博客
- 使用Hexo修改博客样式

## 在GitHub上创建博客
### 创建自己的博客
1. 创建一个新的仓库
![图1-1 创建仓库][1]
2. 设置仓库名
仓库名必须为【你的GitHub名】+【.github】+【.io】如图1-2。
![图1-2 设置仓库信息][2]
3. 定义自己的风格
这里简易定义一些自己的风格，后面会使用Hexo进行重定义，可忽略
在YoRenChen.github.io内的【settings】-【GitHub Pages】修改主题
![图1-3 定义博客主题][3]
4. 访问博客
创建完成之后，在浏览器搜索你的博客名【yorenchen.github.io】
![图1-4 访问博客][4]
5. 修改文件样式
创建之后会发现多出了【config.yml】和【index.md】文件，下载修改主题以及其他样式，再重新上传即可。
![图1-5 下载文件][5]
![修改config样式][6]
## 使用Hexo
使用Hexo需要有git和node环境
### 安装Git
[git官网][7]
安装之后查看版本(命令行)：`- git -v`
安装完成之后，右键会多一个Git bash的选项
### 安装Node.js
[node官网][8]
安装之后查看版本(命令行)：`- node -v`
### 安装Hexo
在需要安放Hexo的文件夹右键git bash
安装hexo: `- npm i hexo-cli -g`
查看版本： `- hexo -v`
### 初始化
`- hexo init`
文件目录：
![][9]
### Hexo 链 GitHub



  [1]: ./images/1533773940444.jpg
  [2]: ./images/1533774251943.jpg
  [3]: ./images/1533774527260.jpg
  [4]: ./images/1533774601002.jpg
  [5]: ./images/1533774712034.jpg
  [6]: ./images/1533774834155.jpg
  [7]: https://gitforwindows.org/
  [8]: https://nodejs.org/en/
  [9]: ./images/1533787124449.jpg