---
title: Changes not staged for commit
date: 2019-10-10 15:39:39
categories: 问题解决
description:  git commit 报 "Changes not staged for commit:"是怎么回事?。
photos: 
    - "http://lonelyi.cn/images/你的名字.jpg"
---
我是clone了一个文件夹下来，然后想把这个文件夹添加到github，commit push到github之后
发现是一个空文件夹
我就git status发现 这个文件还在暂存区
报Changes not staged for commit的错误,解决如下：
因为是clone下来的文件，所以有.git文件，将.git文件删除就ok啦
因为在其他的themes下已经被git管理了到不能提交的目录下
用命令rm -rf .git 移除隐藏的git文件夹，然后到根目录下git init 在执行提交操作就好了