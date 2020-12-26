---
title: git 基本设置
date: 2018-10-17 09:56:23
tags: [git, 乱码]
categories: study
---
### 基本设置
``` sh
git config --global user.email=russellmars@sina.com
git config --global user.email russellmars@sina.com
git config --global core.editor vim
``` 
### 乱码处理
电脑win10 在使用git的时候无论时bash还是cmd或者是vs code里显示的commit message的时候中文都是乱码的。
解决方法，打开bash，依次输入如下命令：
``` bash
git config --global core.quotepath false 
git config --global gui.encoding utf-8
git config --global i18n.commit.encoding utf-8 
git config --global i18n.logoutputencoding utf-8 
export LESSCHARSET=utf-8
```

然后在环境变量里加入`LESSCHARSET=utf-8`，问题解决。
