---
title: Git - 生成 SSH 公钥链接github
date: 2019-10-24 11:24:16
categories: 学习记录
description: 使用SSH方式实现Git远程连接GitHub
tags: Git
---

```shell
// 查看是否存在秘钥
$ cd ~/.ssh
//如果能进入到.ssh文件目录下,说明之前生成过

//查看用户配置的相关信息
git config user.name
git config user.email
如果之前没有创建，执行以下命令
git config –global user.name ‘xxxxx’ 
git config –global user.email ‘xxx@xx.xxx’
// 生成秘钥 (邮箱为上方配置的邮箱)
$ ssh-keygen -t rsa -C ‘xxx@xx.xxx’
// 连按三个回车
Enter file in which to save the key (/c/Users/shiyi/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/shiyi/.ssh/id_rsa.
Your public key has been saved in /c/Users/shiyi/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:vGtH/vwPOz7DycwjJZ/AHlzQuvFjYpG759Yhh1lWGI shiyi_box@163.com
The key"s randomart image is:
+---[RSA 2048]----+
|    +E .         |
| ..+oo+          |
| oo+*+.o         |
|o.*===+o         |
|==+*... S        |
|B.+.o .o         |
|++o. +  .        |
| +o.+ .          |
|.  o.o           |
+----[SHA256]-----+
//最后在.ssh目录下得到了两个文件：id_rsa（私有秘钥）和id_rsa.pub（公有密钥）
//生成后，现在把id_rsa.pub里面的内容复制到githubd 的add github key 的key里面

//Settings
```
![sshGit1](/images/sshGit1.png)
```shell
//点击SSH and GPG keys,创建New SSH key，
```
![sshGit2](/images/sshGit2.png)
```shell
//粘贴你的密钥到你key输入框中
```
![sshGit3](/images/sshGit3.png)
```shell
//点击Add SSH key
//输入你的GitHub密码，点击确认按钮
```


