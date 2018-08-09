---
title: windows下的 tree 生成目录
tags: tree, 生成目录
grammar_cjkRuby: true
---


发现windows系统下也有tree指令，不过这个指令功能目前只有两个：
![][1]
### 基本操作有：`tree (检索路径) /f`
### 打印日志方法： `tree (检索路径) /f >(输出路径)tree.text`
1. 检索路径不输入为默认当前路径
2. 打印日志为打印到tree.text中

### 如果想要windows下也能像linux的强大功能，需要额外安装：
1. `tree-cli`或`treer`(需要node环境)
	安装之后就可以正常操作
2. 使用git bash(需要安装git)
	使用git bash 也能像linux使用tree
	![][2]


  [1]: ./images/1533786114500.jpg
  [2]: ./images/1533786710457.jpg