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
### Hexo 连接 GitHub
连接需要GitHub提供在本地上传文件的权限，也就是SSH Keys。
同时需要在本地生成ssh key。
【设置本地GitHub账户信息绑定】

``` 
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub注册邮箱"
```
【生成ssh key】
``` 
ssh-keygen -t rsa -C "你的GitHub注册邮箱"
```
生成之后在.ssh文件找到对应文件id_rsa.pub（这个为公钥），复制上面内容
![][10]
在[https://github.com/settings/keys][11] 上新建ssh key
![][12]
查询是否成功，本地使用git bash输入`ssh git@github.com`
![][13]
提示以上信息说明成功

### 修改Hexo配置文件
我们尝试性修改文件，并提交到我们的GitHub上。
详细可以查看[hexo部署][14]
【修改配置】
找到文件`_config.yml`修改配置
![][15]
配置上传到对应的地址信息
![][16]
【上传】
那么我们使用什么命令上传呢，先别急。我们hexo上传git需要安装一个小插件：`npm install hexo-deployer-git --save`
执行命令：
创建新的post：` hexo new "My New Post"`
跑服务Run server：`hexo server`
生成静态文件Generate static files：`hexo generate`
发布hexo deploy：`hexo deploy`

成功之后访问GitHub发现文件已经修改
![enter description here][17]
访问[yorenchen的GitHub博客][18]
![enter description here][19]


  [1]: ./images/1533773940444.jpg
  [2]: ./images/1533774251943.jpg
  [3]: ./images/1533774527260.jpg
  [4]: ./images/1533774601002.jpg
  [5]: ./images/1533774712034.jpg
  [6]: ./images/1533774834155.jpg
  [7]: https://gitforwindows.org/
  [8]: https://nodejs.org/en/
  [9]: ./images/1533787124449.jpg
  [10]: ./images/1534511712767.jpg
  [11]: https://github.com/settings/keys
  [12]: ./images/1534511774763.jpg
  [13]: ./images/1534511974640.jpg
  [14]: https://hexo.io/zh-cn/docs/deployment.html
  [15]: ./images/1534512195725.jpg
  [16]: ./images/1534512224391.jpg
  [17]: ./images/1534512808865.jpg
  [18]: https://yorenchen.github.io/
  [19]: ./images/1534512749755.jpg