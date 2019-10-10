---
title: Navicat client安装失败
date: 2019-10-10 14:32:39
categories: 问题解决
description:  Navicat Premium 连接sql server 需要安装client 然而安装过程中报错。
---

这是因为默认安装的是32位，若电脑是64位的，需要去安装目录下执行sqlncli_x64.msi 这个文件



若报错信息
![Navicatclient.png](https://lonelyi.cn/images/Navicatclient.png)

需要安装VC2005，client依赖于它



若安装VC2005依然失败：

报错信息类似 "win32",有可能是sp1没有装，去 https://www.microsoft.com/zh-cn/download/details.aspx?id=5842
下载windows6.1-KB976932-X64.exe安装，若还是安装失败，需要windows检测更新，重启后再安装

